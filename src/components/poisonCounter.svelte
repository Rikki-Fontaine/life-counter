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
    <span>&#x2623;</span>
    <button on:click={decrement}>-</button>
    <span class="count">{count}</span>
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
        display: flex;
        width: fit-content;
        padding: 5px;
        margin: 5px;
    }

    .count{
        margin-left: 1rem;
        margin-right: 1rem;
    }
</style>


