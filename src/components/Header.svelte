<header class="main-header">
    <div class="logo-container">
        <img src="/svelte.svg" alt="" class="logo">
        <div class="title">Svelte Todo List</div>
    </div>
</header>

<style>
    .main-header {
        height: 75px;
        background-color: gray;
        padding: .5rem;
    }

    .logo-container {
        display: flex;
        align-items: center;
        gap: 1rem;
        height: 100%;
        margin-left: 1rem;
        max-width: 30%;
    }

    .logo {
        height: 85%;
        filter: drop-shadow(2px 2px 6px rgb(31, 31, 31))
    }

    .title {
        font-size: 2rem;
        font-weight: bold;
        color: rgb(36, 34, 34);
        text-shadow: 2px 2px 5px rgb(46, 46, 46);
    }

</style>
