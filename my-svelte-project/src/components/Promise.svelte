<script>
    // async function promiseFunc(){
    //     const result = new Promise((resolve, reject) => {
    //         setTimeout(() => {
    //             resolve('Hello Universe~!');
    //         }, 1000);
    //     });
    //     const rtn = await result;
    //     return rtn;
    // }

    async function getPosts(){
        const res = await fetch('https://jsonplaceholder.typicode.com/posts');
        const json = await res.json();
        return json;
    }
    let promisePosts = getPosts();
</script>

<main>
    <!-- {#await promiseFunc()} 
        <h1>잠시만 기다리세요..</h1>
    {:then res} 
        <h1>{res}</h1>
    {:catch error}
        <h1>Error: {error.message}</h1>
    {/await} -->

    <button on:click={() => promisePosts = getPosts()}> 프스트 리스트 가져오기 </button>

    <table border="1">
        <thead>
            <th>id</th>
            <th>사용자</th>
            <th>타이틀</th>
            <th>내용</th>
        </thead>
        <tbody>
            {#await promisePosts}
                <tr>
                    <td colspan=4>
                        가져오는 중 잠시만 기다리세요
                    </td>
                </tr>
            {:then posts} 
                {#each posts as post}
                    <tr>
                        <td>{post.id}</td>
                        <td>{post.userId}</td>
                        <td>{post.title}</td>
                        <td>{post.body}</td>
                    </tr>
                {/each}
            {/await}
        </tbody>
    </table>
</main>