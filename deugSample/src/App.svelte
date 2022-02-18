<script>
	export let name = 'world';
</script>

<input type="text" bind:value={name} />

{@debug name}

<h1>Hello {name}!</h1>
