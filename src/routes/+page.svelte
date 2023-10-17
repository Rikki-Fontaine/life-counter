<script>
    import LifeCounter from "../components/lifeCounter.svelte";
    import PoisonCounter from "../components/poisonCounter.svelte";
    import CmndCounter from "../components/cmndCounter.svelte";
    import Display from "../components/display.svelte";
  import CommandDisplay from "../components/commandDisplay.svelte";
    export let theme = "gruul"

</script>

<h1>Magic Life Counter (work in progress)</h1>

<main class = {theme}>
    <Display colors= {theme} > 
        <div class="themeMenu">  <!--Buttons with functions to change the theme variable to reassign the class name-->
            <p>Theme:</p>
            <button on:click={() => theme = "azorius"}>Azorius</button>
            <button on:click={() => theme = "gruul"}>Gruul</button>
            <button on:click={() => theme = "rakdos"}>Rakdos</button>
        </div>
        <LifeCounter>
        </LifeCounter>
        <PoisonCounter />
        <CommandDisplay>
            <CmndCounter />
            <CmndCounter />
            <CmndCounter />
        </CommandDisplay>
        
    </Display>
</main>

<style>
    main{
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: black;
        border: solid 2px red;
        left: 50%;
        top: 50%;
        transform: translate(-50%,-50%);
    }
    
    .themeMenu{
        display: flex;
        justify-content: center;
        gap: 3rem;
    }
    
    .gruul{
        background-color: green;   
    }

    .azorius{
        background-color: white;
    }

    .rakdos{
        background-color: black;
    }

    h1{
        text-align: center;
        color : black;
    }

   
</style>