<div class="card">
    <slot />
</div>

<style>
    .card {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 1rem;
        font-family: 'Poppins', sans-serif;
        background-color: white;
        border-radius: .5rem;
        box-shadow: 2px 2px 6px gray;
        padding: 10px 20px;
        margin: 20px 0;
    }
</style>