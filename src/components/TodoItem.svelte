<script>
    import { createEventDispatcher } from 'svelte'
    import Button from "./Button.svelte";
    import Card from "./Card.svelte";

    const dispatch = createEventDispatcher()

    export let text
    export let id
    // export let completed

    const deleteTodo = () => dispatch('delete', id)
    
</script>

<Card>
    <p>{text}</p>
    <div class="buttons-wrapper">
        <Button on:forwardclick={deleteTodo}>Delete</Button>
        <Button>Archive</Button> 
    </div>
</Card>