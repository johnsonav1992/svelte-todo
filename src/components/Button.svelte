<script>
    export let rightRounded;
</script>

<button class="button {rightRounded}"  >
    <slot />
</button>

<style>
    .button {
        border: none;
        border-radius: .5rem;
        background-color: #fb3d07;
        font-family: 'Poppins', sans-serif;
        font-size: 1rem;
        height: 2rem;
        color: white;
        cursor: pointer;
        transition: all 200ms ease;
    }

    .button:hover {
        background-color: rgb(207, 50, 6);
    }

    .btn-right-rounded {
        border-top-right-radius:  .5rem;
        border-bottom-right-radius: .5rem;
        border-top-left-radius: 0;
        border-bottom-left-radius: 0;
    }
</style>