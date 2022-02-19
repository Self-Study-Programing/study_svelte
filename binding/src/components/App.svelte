<script>
	let name = 'world';
	let size = 30;
</script>


<main>
	<input type="range" bind:value={size} min=0 max=100 /><br />
	<input type="number" bind:value={size} min=0 max=100 /><br />
	<input type="text" bind:value={name} />

	<h1>Hello {name}!</h1>
</main>