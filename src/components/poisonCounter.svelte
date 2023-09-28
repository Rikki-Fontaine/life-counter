<script>
    

	let count = 0;

	function increment() {
		count += 1;
	};

    function decrement() {
		count -= 1;
	};
</script>

<div class="container">
    <span>&#9763;</span>
    <button on:click={decrement}>-</button>
    <span>{ count}</span>
    <button on:click={increment}>+</button>
</div>


<style>
    button {
        color : black;
        background-color: lightgreen;
        font-weight: bolder;
        
    }

    span{
        font-weight: bolder;
        margin: 10px;
    }

    .container {
        width: fit-content;
        padding: 5px;
        margin: 5px;
    }
</style>


