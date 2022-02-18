<script>
    let man = {
        age: 10,
        name: {first: '승현', last: '박'}
    };

    let name = man.name;
    
    function assignment(){
        man.name.last = 'park';
        console.log(name.last);
        name = name;
    }
</script>

<p>man.name.last: {man.name.last}</p>
<p>name.last: {name.last}</p>
<button on:click={assignment}>할당</button>