<script>
	let a = 1;
</script>

<input type="number" bind:value={a} />

{#if a == 0}
	<p>{a} 입니다.</p>
{:else if a > 0}
	<p>{a} 은(는) 양수입니다.</p>
{:else}
	<p>{a} 은(는) 음수입니다.</p>
{/if}

<style>

</style>