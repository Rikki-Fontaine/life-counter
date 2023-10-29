<script>
import {life} from '../store'

function lifeTwenty(){
    life.set(20)
}

function lifeThirty(){
    life.set(30)
}

function lifeFourty(){
    life.set(40)
}

    let lifeTotal;
    const unsubscribe = life.subscribe((value) => {
		lifeTotal = value;
	});
</script>

<div class="input-field">
    <span>Set Life:</span>
    <button on:click={lifeTwenty}>
        20
    </button>

    <button on:click={lifeThirty}>
        30
    </button>

    <button on:click={lifeFourty}>
        40
    </button>
</div>

<style>
    .input-field{
        display: flex;
        justify-content: space-around;
        margin-bottom: 4rem;
        gap: 2rem;
        margin-top: 3rem;
    }

    button{
        background-color: black;
        color: white;
    }

    
</style>