<script>
    import TodoItem from '../components/TodoItem.svelte'
</script>

<div class="todo-list">
    <!-- {#each todo as todoItem (id)} -->
        <TodoItem />
    <!-- {/each} -->
</div>