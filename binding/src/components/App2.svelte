<script>
    let editable = false;
    let favorite = '스벨트';
</script>

<main>
    <input type="checkbox" bind:checked={editable} />
    {#if  editable}
        <p>수정 모드: <input bind:value={favorite} /></p>
    {:else}
        <p>보기 모드: {favorite}</p>
    {/if}
</main>