<script>
    let name = 'world';
</script>

<input type="text" bind:value={name} />

<p>{Date()}</p>

{#key name}
    <p>{Date()}</p>
    <h1>Hello {name}</h1>
{/key}

