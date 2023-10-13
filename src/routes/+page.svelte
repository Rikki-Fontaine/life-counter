<script>
    import LifeCounter from "../components/lifeCounter.svelte";
    import PoisonCounter from "../components/poisonCounter.svelte";
    import CmndCounter from "../components/cmndCounter.svelte";
    import Display from "../components/display.svelte";
   

</script>

<h1>Magic Life Counter (work in progress)</h1>
<main>
    <Display colors={null} > <!--This has a colors prop I should be able to use to pass theme data to the display to match it to main-->
        <LifeCounter>
        </LifeCounter>
        <PoisonCounter />
        <CmndCounter />
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
    
    h1{
        text-align: center;
        color : black;
    }

   
</style>