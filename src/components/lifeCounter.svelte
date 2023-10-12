<script>
	let count = 0;

    const setLife20 = () => {
        count = 20
    };
    
    const setLife30 = () => {
        count = 30
    }; 

    const setLife40 = () => {
        count = 40
    }; 

	const increment = () => {
		count += 1;
	};

    const decrement = () => {
		count -= 1;
	};
</script>

<div class="input-field">
    <button on:click={setLife20}>
        Standard
    </button>

    <button on:click={setLife30}>
        2 Headed Giant
    </button>

    <button on:click={setLife40}>
        Commander
    </button>
</div>


<div class="container">
    <span>&#9829;</span>
    <button on:click={decrement}>-</button>
    <span>{count}</span>
    <button on:click={increment}>+</button>
</div>

<style>
    button {
        color : white;
        background-color: black;
        font-weight: bolder;
    }

    span{
        font-weight: bolder;
        margin: 10px;
    }

    input{
        color: wheat;
    }

    .container {
        display: flex;
        width: fit-content;
        padding: 5px;
        margin: 5px;
    }

    .input-field{
        display: flex;
        justify-content: space-around;
        margin-bottom: 4rem;
        gap: 2rem;
    }
</style>