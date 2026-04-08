<script>
    let todos = $state([
        { title: "Assignemnt 1", done: false},
        { title: "Assignemnt 2", done: true},
        { title: "Assignemnt 3", done: false}
    ])
</script>

<h3>My Todos</h3>

<ul>
    {#each todos as todo}
        <li>
            <input type="checkbox" bind:checked={todo.title}>
            {todo.title}
        </li>
    {/each}
</ul>