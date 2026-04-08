<script>
    let todos = $state([
        { title: "Assignemnt 1", done: false},
        { title: "Assignemnt 2", done: false},
        { title: "Assignemnt 3", done: false}
    ])
</script>

<h3>My Todos</h3>

<ul>
    {#each todos as todo}
        <li>{todo.title}</li>
    {/each}
</ul>