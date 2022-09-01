<button class="button">
    <slot />
</button>

<style>
    .button {
        border: none;
        background-color: #fb3d07;
        border-top-right-radius:  .5rem;
        border-bottom-right-radius: .5rem;
        font-family: 'Poppins', sans-serif;
        color: white;
        padding: 10px 15px;
        font-size: 20px;
        -webkit-appearance: none;
        cursor: pointer
    }

    .button:hover {
        background-color: #f8572b;
    }
</style>