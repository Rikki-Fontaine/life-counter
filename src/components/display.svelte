<script>
    export let colors = theme;
</script>

<div class={colors}>
    <slot/>
</div>

<style>
        div{
        display: flex;
        flex-direction: column;
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%,-50%);
        border: solid 4px blue;
        padding: 10px;
        
        width: 75%;
        height: 100%;
        align-items: center;
        padding: 1rem;

    }

    .gruul{
        background-color: red;
    }

    .azorius{
        background-color: blue;
    }

    .rakdos{
        background-color: red;
    }
</style>