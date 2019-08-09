<script>
  export let name;
</script>

<style>

</style>

<div class="container mx-auto py-10 flex flex-col items-center">
  <img class="w-56 object-center" src={'/img/app-logo.svg'} alt="" />
  <div class="w-1/2 my-5">
    <form class="w-full focus-within:border-teal-500">
      <div class="flex items-center border-b border-b-2 py-2">
        <input
          class="appearance-none bg-transparent border-none w-full text-gray-700
          mr-3 py-1 px-2 leading-tight focus:outline-none"
          type="text"
          placeholder="Jane Doe"
          aria-label="Full name" />
        <button
          class="flex-shrink-0 bg-purple hover:bg-purple border-purple
          hover:border-pruple text-sm border-4 text-white py-1 px-2 rounded"
          type="button">
          Add
        </button>
      </div>
    </form>
  </div>
  <div class="w-1/2 flex flex-col items-center">
    <ul class="list">
      <li class="list-item">
        <input type="checkbox" class="hidden-box" id="first" checked />
        <label for="first" class="check--label">
          <span class="check--label-box" />
          <span class="check--label-text">First Checkbox</span>
        </label>
      </li>
      <li class="list-item">
        <input type="checkbox" class="hidden-box" id="second" />
        <label for="second" class="check--label">
          <span class="check--label-box" />
          <span class="check--label-text">Second Checkbox</span>
        </label>
      </li>
      <li class="list-item">
        <input type="checkbox" class="hidden-box" id="third" />
        <label for="third" class="check--label">
          <span class="check--label-box" />
          <span class="check--label-text">Third Checkbox</span>
        </label>
      </li>
    </ul>
  </div>

</div>
