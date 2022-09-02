<script>
    import Button from "./Button.svelte";

</script>

<form on:submit|preventDefault type="submit" class="todo-form">
    <input type="text" name="todo-input" class="todo-input" placeholder="Add a todo"><Button rightRounded="btn-right-rounded" >Add</Button>
</form>

<style>
    .todo-form {
        padding: 2rem;
    }
    .todo-input {
        font-family: 'Poppins', sans-serif;
        font-size: 1rem;
        padding: .5rem;
        border: none;
        height: 2rem;
        min-width: 300px;
        border-top-left-radius: .5rem;
        border-bottom-left-radius: .5rem;
    }

    .todo-input:hover {
        background-color: rgb(249, 244, 244);
    }

    .todo-input:focus {
        outline: none;
    }

</style>