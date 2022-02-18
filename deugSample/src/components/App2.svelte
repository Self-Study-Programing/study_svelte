<script>
    let colors = ['빨강', '주황', '노랑', '초록'];

    $: console.log('log.1: ', colors);

    function assignment(){
        colors.pop();
        colors = colors;
        console.log('log.2: ', colors);
    }
</script>

<p>{colors.join(', ')} 모두 {colors.length} 개의 색이 있습니다.</p>
<button on:click={assignment}>할당</button>