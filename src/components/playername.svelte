<script>
       let name = "";
    let playerName = false
</script>





<input class={playerName ? "hidden" : ""} bind:value={name} placeholder="enter your name" /> <button class={playerName ? "hidden" : ""} on:click={() => playerName = !playerName}>OK</button>
    <p class={playerName ? "up" : ""}>{name || ""}</p>

    <style>
    .up{
        transform: translateY(-50px);
    }

    .hidden{
        visibility: hidden;
    }

    input{
        color: black;
    }

    p{
        font-weight: bolder;
        font-size: larger;
    }

    button {
        color : white;
        background-color: black;
        font-weight: bolder;
    }
    </style>