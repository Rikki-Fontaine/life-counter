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

<div class="lifeHolder">
    

    

<!-- The Items above need to be put into their own components and still able to perform their function-->


    <div class="container">
        <span class="heart">&#9829;</span>
        <button on:click={decrement}>-</button>
        <span>{lifeTotal}</span>
        <button on:click={increment}>+</button>
    </div>
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
        width: fit-content;
        padding: 5px;
        margin: 5px;
    }



    .lifeHolder{
        display: block;
    }
</style>