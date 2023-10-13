<script>
	let count = 0;
    let name = "";
    let playerName = false
    
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
    <span>Set Life:</span>
    <button on:click={setLife20}>
        20
    </button>

    <button on:click={setLife30}>
        30
    </button>

    <button on:click={setLife40}>
        40
    </button>
</div>

<input class={playerName ? "hidden" : ""} bind:value={name} placeholder="enter your name" /> <button class={playerName ? "hidden" : ""} on:click={() => playerName = !playerName}>OK</button>
<p class={playerName ? "up" : ""}>{name || ""}</p>

<div class="container">
    <span class="heart">&#9829;</span>
    <button on:click={decrement}>-</button>
    <span>{count}</span>
    <button on:click={increment}>+</button>
</div>

<style>
    .up{
        transform: translateY(-50px);
    }

    .hidden{
        visibility: hidden;
    }

    button {
        color : white;
        background-color: black;
        font-weight: bolder;
    }

    span{
        font-weight: bolder;
        margin: 10px;
    }

    .heart{
        font-size: large;
    }

    p{
        font-weight: bolder;
        font-size: larger;
    }

    input{
        color: black;
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
        margin-top: 3rem;
    }
</style>