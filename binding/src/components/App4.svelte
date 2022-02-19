<script>
    let where = ''; // radio 그룹 바인딩 변수
    let menu = ['커피', '주스', '샌드위치', '김밥']; // 메뉴를 담은 배열
    let chosen = [];
    let order = "";
    $:order = chosen.length > 0 ? `<b>${chosen}</b> 메뉴를 <b>${where=='매장'?'매장 식사를':'포장 주문을'}</b> 선택하셨습니다`:'메뉴를 선택해주세요.';
</script>

<main>
    <h2>포장: {where}</h2>
    <input type="radio" name="" id="" bind:group={where} value="포장"> 포장합니다
    <input type="radio" name="" id="" bind:group={where} value="매장"> 매장에서 먹을래요

    <h2>메뉴: {chosen}</h2>
    {#each menu as item}
        <label>
            <input type="checkbox" bind:group={chosen} value={item}> {item}
        </label>
    {/each}

    <p>{@html order}</p>
</main>