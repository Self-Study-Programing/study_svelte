<script>
    let where = '';
</script>

<main>
    <h2> 포장: {where}</h2>
    <input type="radio" bind:group={where} value="포장"> 포장합니다
    <input type="radio" bind:group={where} value="매장"> 매장에서 먹을래요
</main>