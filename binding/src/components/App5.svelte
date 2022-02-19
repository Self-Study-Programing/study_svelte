<script>
    import { marked } from 'marked'
    let markdown = "# 타이틀 \n\n- 리스트1\n- 리스트 \n- 리스트3";
</script>

<textarea bind:value={markdown} placeholder="내용 입력" />

<div class="preview">{@html marked(markdown)}</div>

<style>
    textarea{
        height: 40%;
        widows: 100%;
        margin: 0;
        border: none;
    }

    .preview {
        height: 60%;
        padding: 20px;
        border-top: solid 2px gray;
    }
</style>