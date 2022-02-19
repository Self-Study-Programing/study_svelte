<script>
    let html = "<p>가장 빨리 만나는 스벨트</p>";
</script>

<div contenteditable="true" bind:innerHTML={html}></div>
<pre>{html}</pre>

<style>
    [contenteditable=true]{
        padding: 0.5rem;
        border: 1px solid #eee;
        border-radius: 10px;
    }
</style>