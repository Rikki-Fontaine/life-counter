<script>
	let count = 0;

	function increment() {
		count += 1;
	};

    function decrement() {
		count -= 1;
	};
</script>

<span>Poison:</span>
<button on:click={decrement}>-</button>
<span>{count}</span>
<button on:click={increment}>+</button>



<style>
    button {
        color : black;
        background-color: lightgreen;
        font-weight: bolder;
    }
</style>


