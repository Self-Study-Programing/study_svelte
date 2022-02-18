<script>
	let count = 0; // 반응형 변수 선언

	$: console.log(`1. 한 줄 구문: ${count}`); // 동작 정의

	$: {
		count;
		console.log('2. 코드 블록: count가 변경됨');
	}

	$: if(count>0){
		console.log('3. if 조건: count가 0보다 크다')
	}

	$: for(let i = 0; i<4; i++){
		count;
		console.log('4. for loop 안에 count 값 변경됨 for: ', i)
	}

	function addCount(){
		count = count + 1;
	}
</script>

<button on:click={addCount}>카운트는 {count}입니다</button>