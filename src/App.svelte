<script>
  // @ts-ignore
import Tailwindcss from "./Tailwindcss.svelte";
let keyword
let FormEntered = (event)=>{
  event.preventDefault()
  location.href = `https://search.naver.com/search.naver?where=nexearch&sm=top_hty&fbm=1&ie=utf8&query=${keyword}`
}

</script>
<Tailwindcss/>
<main>
  <div>
    <form action="get" class="grid" on:submit={FormEntered}>
      <input type="text" bind:value = {keyword} class="bg-white justify-self-center rounded-lg w-96 h-10 mt-56 font-sans focus: outline-none caret-slate-400 hover:border-lime-400 border-2">
      <input type="submit" class="invisible">
    </form>
  </div>
</main>

<style>
  :global(body){
    background-color: #34d399;
  }
</style>
