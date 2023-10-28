<script>
import {life} from '../store'

const setLife20 = () => {
    count = 20
};

const setLife30 = () => {
    count = 30
}; 

const setLife40 = () => {
    count = 40
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