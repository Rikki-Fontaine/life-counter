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
                <button class="azoriusBtn" on:click={() => theme = "azorius"}>Azorius</button>
                <button class="gruulBtn" on:click={() => theme = "gruul"}>Gruul</button>
                <button class="rakdosBtn" on:click={() => theme = "rakdos"}>Rakdos</button>
                <button class="simicBtn" on:click={() => theme = "rakdos"}>Simic</button>
                <button class="golgariBtn" on:click={() => theme = "rakdos"}>Golgari</button>
                <button class="selesnyaBtn" on:click={() => theme = "rakdos"}>Selesnya</button>
                <button class="dimirBtn" on:click={() => theme = "rakdos"}>Dimir</button>
                <button class="borosBtn" on:click={() => theme = "rakdos"}>Boros</button>
                <button class="izzetBtn" on:click={() => theme = "rakdos"}>Izzet</button>
                <button class="orzhovBtn" on:click={() => theme = "rakdos"}>Orzhov</button>
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
        justify-content: center;
        gap: 1rem;
        background-color: black;
        opacity: 100%;
        height: 70%;
        width: 50%;
        border-radius: 5%;
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

    .rakdosBtn{
        background-image: linear-gradient(#121212, #F05454);
    }

    .simicBtn{
        background-image: linear-gradient(#2192FF, #38E54D)
    }

    .golgariBtn{
        background-image: linear-gradient(#347A2A, #121212)
    }

    .selesnyaBtn{
        background-image: linear-gradient(#FCF9F9, #7CBD1E)
    }

    .borosBtn{
        background-image: linear-gradient(#DD3E3E, #F2F2F2)
    }

    .izzetBtn{
        background-image: linear-gradient(#3F52E3, #F12D2D)
    }

    .dimirBtn{
        background-image: linear-gradient(#121212, #00A9FF )
    }

    .orzhovBtn{
        background-image: linear-gradient(#121212, #F2F2F2);
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