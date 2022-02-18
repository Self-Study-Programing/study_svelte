<script>
    let colors = ['빨강', '노랑', '파랑', '보라'];
</script>

<main>
    <select name="" id="">
        {#each colors as color, idx}
            <option> {idx + 1}: {color} </option>
        {/each}
    </select>
    <ul>
        {#each colors as color, idx}
            <li>{idx}: {color}</li>
        {/each}
    </ul>
</main>