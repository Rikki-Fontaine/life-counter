<script>
    import LifeCounter from "./lifeCounter.svelte";
    export let lifeCount = count; //Pay attention here, this may not work how I'm thinking.
    

    export const setLife20 = () => {
        lifeCount = 20
    };
    
    export const setLife30 = () => {
        lifeCount = 30
    }; 

    export const setLife40 = () => {
        lifeCount = 40
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