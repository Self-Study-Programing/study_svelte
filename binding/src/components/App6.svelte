<script>
    let choice = [];
    $:console.log(choice);
</script>

<select multiple bind:value={choice}>
    <option value="값1"> 값1 선택 </option>
    <option value="값2"> 값2 선택 </option>
    <option value="값3"> 값3 선택 </option>
</select>