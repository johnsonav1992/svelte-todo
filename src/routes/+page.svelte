<script>
    import { v4 as uuidv4 } from 'uuidv4'
    import Input from '../components/Input.svelte'
    import TodoList from '../components/TodoList.svelte';
    import Container from '../components/Container.svelte'
    import TodoItem from '../components/TodoItem.svelte';

    let todoItems = [
        {
            id: uuidv4(),
            text: 'Clean the house',
            completed: false
        },
        {
            id: uuidv4(),
            text: 'Make kimchi',
            completed: false
        },
        {
            id: uuidv4(),
            text: 'Code some awesome projects',
            completed: false
        }
    ]

    function addTodoHandler(e) {
        let newTodo = e.detail 

    }
</script>

<Container>
    <Input on:addTodo={addTodoHandler} />
    <TodoList> 
        {#if todoItems.length === 0}
            <p>There are no todos!</p>
        {:else}
            {#each todoItems as todo (todoItems.id)}
            <TodoItem text={todo.text}/>
            {/each}
        {/if}
    </TodoList>
</Container>

