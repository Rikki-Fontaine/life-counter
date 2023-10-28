<script>
    import {life} from '../store'
    let name = "";
    let playerName = false
    

	const increment = () => {
		lifeTotal += 1;
	};

    const decrement = () => {
		lifeTotal -= 1;
	}; 

    let lifeTotal;
    const unsubscribe = life.subscribe((value) => {
		lifeTotal = value;
	});
    
</script>

<div class="lifeHolder">
    

    <input class={playerName ? "hidden" : ""} bind:value={name} placeholder="enter your name" /> <button class={playerName ? "hidden" : ""} on:click={() => playerName = !playerName}>OK</button>
    <p class={playerName ? "up" : ""}>{name || ""}</p>

<!-- The Items above need to be put into their own components and still able to perform their function-->


    <div class="container">
        <span class="heart">&#9829;</span>
        <button on:click={decrement}>-</button>
        <span>{lifeTotal}</span>
        <button on:click={increment}>+</button>
    </div>
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

    .lifeHolder{
        display: block;
    }
</style>