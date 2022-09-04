<script>
    import {v4 as uuidv4} from 'uuid'
    import Button from "./Button.svelte";
    import { createEventDispatcher } from 'svelte'

    const dispatch = createEventDispatcher()

    function submitTodo(e) {
        let newTodo = {
            id: uuidv4(),
            text: e.target[0].value,
            completed: false
        }
        
        dispatch('addTodo', newTodo)

        e.target[0].value = ''
    }
</script>

<form on:submit|preventDefault={submitTodo} type="submit" class="todo-form" >
    <input type="text" 
        name="todo-input" 
        class="todo-input" 
        placeholder="Add a todo" 
    ><Button rightRounded="btn-right-rounded" >Add</Button>
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