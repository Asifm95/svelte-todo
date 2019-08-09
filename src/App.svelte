<script>
  let newTodo = "";
  let todos = [
    {
      id: 1,
      title: "buy mangos",
      completed: false
    },
    {
      id: 2,
      title: "buy bananas",
      completed: false
    },
    {
      id: 3,
      title: "buy beer today",
      completed: false
    }
  ];

  const addTodo = () => {
    if (newTodo) {
      todos = [
        ...todos,
        {
          id: todos.length + 1,
          title: newTodo,
          completed: false
        }
      ];
      newTodo = "";
    }
  };
</script>

<style>

</style>

<div class="container mx-auto py-10 flex flex-col items-center">
  <img class="w-56 object-center" src={'/img/app-logo.svg'} alt="logo" />
  <div class="w-1/2 my-5">
    <div class="w-full focus-within:border-teal-500">
      <div class="flex items-center border-b border-b-2 py-2">
        <input
          class="appearance-none bg-transparent border-none w-full text-gray-700
          mr-3 py-1 px-2 leading-tight focus:outline-none"
          type="text"
          placeholder="Jane Doe"
          bind:value={newTodo}
          on:keydown={event => {
            if (event.which == 13) addTodo();
          }} />
        <button
          class="w-10 flex-shrink-0 bg-purple hover:bg-purple border-purple
          hover:border-pruple text-sm border-4 text-white py-1 px-2 rounded"
          type="button"
          on:click={addTodo}>
          +
        </button>
      </div>
    </div>
  </div>
  <div class="w-1/2 flex flex-col items-center">
    <ul
      class="list flex flex-col w-full m-0 p-0 rounded overflow-hidden
      border-solid border border-gray-400">
      {#each todos as todo}
        <li class="list-item border-b border-b-solid border-b-gray-400">
          <input type="checkbox" class="hidden-box" id={todo.id} />
          <label for={todo.id} class="check-label">
            <span class="check-label-box" />
            <span class="check-label-text">{todo.title}</span>
          </label>
        </li>
      {/each}
    </ul>
  </div>

</div>
