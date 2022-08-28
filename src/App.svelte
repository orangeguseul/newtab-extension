<script>
  // @ts-ignore
import Tailwindcss from "./Tailwindcss.svelte";
import Favorites from "./favorite.svelte";
let keyword
let FormEntered = (event)=>{
  event.preventDefault()
  location.href = `https://www.google.co.kr/search?q=${keyword}`
}// google:https://www.google.co.kr/search?q=
// naver:https://search.naver.com/search.naver?where=nexearch&sm=top_hty&fbm=1&ie=utf8&query=

</script>
<Tailwindcss/>
<main>
  
    <form action="get" class="grid" on:submit={FormEntered}>
      <input type="text" bind:value = {keyword} class="bg-white justify-self-center rounded-lg w-96 h-10 mt-56 font-sans border-slate-400 border-2 focus: outline-none caret-slate-400">
      <input type="submit" class="invisible">
    </form>
  <Favorites/>
</main>

<style>
  :global(body){
    background-color: #34d399;
  }
  
</style>
