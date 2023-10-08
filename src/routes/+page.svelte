<script>
    import LifeCounter from "../components/lifeCounter.svelte";
    import PoisonCounter from "../components/poisonCounter.svelte";
    import CmndCounter from "../components/cmndCounter.svelte";
</script>

<h1>Magic Life Counter (work in progress)</h1>
<main>
    
    <div class="display">
        <LifeCounter />
        <PoisonCounter />
        <CmndCounter />
    </div>
</main>

<style>
    main{
        position: absolute;
        width: 50%;
        height: 50%;
        background-color: black;
        border: solid 2px red;
        left: 50%;
        top: 50%;
        transform: translate(-50%,-50%);
    }
    
    h1{
        text-align: center;
        color : black;
    }

    .display{
        display: flex;
        flex-direction: column;
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%,-50%);
        border: solid 4px blue;
        padding: 10px;
        background-color: aqua;
        width: 50%;
        align-items: center;
    }
</style>