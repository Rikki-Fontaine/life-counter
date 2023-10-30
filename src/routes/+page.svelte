<script>
    import LifeCounter from "../components/lifeCounter.svelte";
    import PoisonCounter from "../components/poisonCounter.svelte";
    import CmndCounter from "../components/cmndCounter.svelte";
    import Display from "../components/display.svelte";
    import CommandDisplay from "../components/commandDisplay.svelte";
    import CounterDisplay from "../components/counterDisplay.svelte";
    import SetLife from "../components/setLife.svelte";
    import Playername from "../components/playername.svelte";
    export let theme = "gruul"
    let open = false;
</script>

<h1>Magic Life Counter (work in progress)</h1>

<main class = {theme}>
    <Display colors= {theme} >
        
        <!-- The themeMenu will be made into a dropdown.-->
        <button class="themeBtn" on:click={() => (open = !open)}>Themes:</button>
        {#if open}
            <div class="themeMenu">  <!--Buttons with functions to change the theme variable to reassign the class name-->
                <p>Theme:</p>
                <button class="azoriusBtn" on:click={() => theme = "azorius"}>Azorius</button>
                <button class="gruulBtn" on:click={() => theme = "gruul"}>Gruul</button>
                <button class="rakdosBtn" on:click={() => theme = "rakdos"}>Rakdos</button>
                <button class="simicButton" on:click={() => theme = "rakdos"}>Simic</button>
            </div>
        {/if}

        <SetLife/>
        <Playername/>

       <div class = "counterContainer">
            <LifeCounter />
            <PoisonCounter />
        </div>

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
        position: absolute;
        top: 25%;
        display: flex;
        flex-direction: column;
        gap: 1rem;
        background-color: black;
        opacity: 100%;
        height: 50%;
        width: 50%;
        border-radius: 10%;
        animation: fadeIn .3s;
    }
    
    @keyframes fadeIn{
         0% { opacity: 0; }
        100% { opacity: 100; }
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

    .themeBtn{
        margin-top: 1rem;
    }

    .azoriusBtn{
        background-image: linear-gradient( #F3F9FB, #226597);
    }

    .gruulBtn{
        background-image: linear-gradient(#799351, #AA3A3A);
    }

    h1{
        text-align: center;
        color : black;
    }

    .counterContainer{
        display: flex;
        justify-content: space-around;
    }
   
</style>