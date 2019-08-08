<script>
  export let name;
</script>

<style>

</style>

<div class="container mx-auto py-10 flex flex-col items-center">
  <img class="w-56 object-center" src={'/img/app-logo.svg'} alt="" />
  <div class="w-1/2 my-5">
    <form class="w-full">
      <div class="flex items-center border-b border-b-2 py-2">
        <input
          class="appearance-none bg-transparent border-none w-full text-gray-700
          mr-3 py-1 px-2 leading-tight focus:outline-none"
          type="text"
          placeholder="Jane Doe"
          aria-label="Full name" />
        <button
          class="flex-shrink-0 bg-teal-500 hover:bg-teal-700 border-teal-500
          hover:border-teal-700 text-sm border-4 text-white py-1 px-2 rounded"
          type="button">
          Add
        </button>
      </div>
    </form>
  </div>

</div>
