<script>
    import { v4 as uuidv4 } from 'uuid'
    import Input from '../components/Input.svelte'
    import TodoList from '../components/TodoList.svelte';
    import Container from '../components/Container.svelte'
    import TodoItem from '../components/TodoItem.svelte';



    let todoItems = [
    ]

    function addTodoHandler(e) {
        let newTodo = e.detail
        todoItems = [...todoItems, newTodo]
        console.log(todoItems)

    }

    function deleteTodo(e) {
        console.log(e.detail)
        todoItems = todoItems.filter(todoItem => todoItem.id != e.detail)
    }

</script>

<Container>
    <Input on:addTodo={addTodoHandler} />
    <TodoList> 
        {#if todoItems.length === 0}
            <p>There are no todos!</p>
        {:else}
            {#each todoItems as todo (todo.id)}
            <TodoItem text={todo.text} id={todo.id} on:delete={deleteTodo}/>
            {/each}
        {/if}
    </TodoList>
</Container>

