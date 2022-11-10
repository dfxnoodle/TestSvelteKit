<script>
import TodoForm from "../components/TodoForm.svelte";
import Todo from "../components/Todo.svelte";
import {todos} from "../stores/todoStore.js"
</script>

<main>
    <h1 class="text-2xl font-bold text-center text-gray-800">我要做的</h1>
    <h1 class="text-2xl font-bold text-center text-gray-800">Att göra</h1>
    <h1 class="text-2xl font-bold text-center text-gray-800">Machen</h1>
    <TodoForm/>
    {#each $todos as todo}
        <Todo todo={todo} index={todo.id}/>
    {/each}
</main>
