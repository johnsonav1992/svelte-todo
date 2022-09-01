<script>
    import Button from "./Button.svelte";
</script>

<form type="submit" class="todo-form">
    <input type="text" name="todo-input" class="todo-input" placeholder="Add a todo">
    <Button>Add</Button>
</form>

<style>
    .todo-input {
        display: inline-block;
        border: none;
        padding: 10px 15px;
        font-size: 20px;
        -webkit-appearance: none;
    }

    .todo-input:hover {
        background-color: rgb(249, 244, 244);
    }

    .todo-input:focus {
        outline: none;
    }
</style>