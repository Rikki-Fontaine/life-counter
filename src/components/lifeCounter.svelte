<script>
    import {life} from '../store'
 
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


    <div class="container">
        <span class="heart">&#9829;</span>
        <button on:click={increment}>+</button>
        <span>{lifeTotal}</span>
        <button on:click={decrement}>-</button>
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

    .heart{
        font-size: large;
    }

    .container {
        display: flex;
        flex-direction: column;
        width: fit-content;
        padding: 5px;
        margin: 5px;
        margin-right: 5px;
        text-align: center;
    }
</style>