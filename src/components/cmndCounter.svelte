<script>
    export let opponent = ""
    export let opName = "opNameHidden"
    export let textBox = "textBoxVisible"
    export let okBtn = "okBtnVisible"
	let count = 0;

	function increment() {
		count += 1;
	};

    function decrement() {
		count -= 1;
	};
</script>

<div class="container">
    <input bind:value={opponent} placeholder="opponent name" class={textBox}><button class={okBtn} {textBox} on:click={() => opName = "opNameVisible"}  on:click={() => textBox = "textBoxHidden"} on:click={() => okBtn = "okBtnHidden"}>OK</button>
    <span class={opName}>{opponent}</span>
    <button on:click={decrement}>-</button>
    <span>{count}</span>
    <button on:click={increment}>+</button>
</div>


<style>
    button {
        color : black;
        background-color: yellowgreen;
        font-weight: bolder;
    }

    span{
        font-weight: bolder;
        margin: 10px;
    }

    .container {
        display: flex;
        width: fit-content;
        padding: 5px;
        margin: 5px;
    }

    .opNameHidden{
        display: none;
    }

    .opNameVisible{
        display: block;
    }

    .textBoxHidden{
        display: none;
    }

    .textBoxVisible{
        display: block;
    }

    .okBtnVisible{
        display: block;
        margin-right: 1rem;
    }

    .okBtnHidden{
        display: none;
    }

    input{
        width: 50%;
    }
</style>
