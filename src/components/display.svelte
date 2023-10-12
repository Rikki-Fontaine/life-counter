<div class="display">
    <slot/>
</div>

<style>
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
        width: 75%;
        height: 75%;
        align-items: center;
    }
</style>