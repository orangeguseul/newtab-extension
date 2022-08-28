<script>
  let favorites = [{name:'google',url:'www.google.com'}, {name:'naver',url:'www.naver.com'}, {name:'youtube',url:'www.youtube.com'}];
</script>

<main>
  <div class="grid">
    <div class="grid grid-cols-2 w-7/12 justify-self-center mt-6 sm:grid-cols-2  gap-5 md:grid-cols-3 lg:grid-cols-4 lg:gap-10 lg:w-1/3">
      {#each favorites as favorite}
        <div class="bg-slate-200 w-32 h-20 text-center grid justify-items-center rounded-lg click-motion lg:w-32" style="background-color: hsl(226, 232%, 240% ,0.5) ">
          <a href="https://{favorite.url}" style="opacity: 1" class="mt-2">
            <img src="https://{favorite.url}/favicon.ico" alt="{favorite.name}" class="w-10 h-10 justify-self-center mr-10 ml-10" style="opacity: 1"/>{favorite.name}
          </a>
        </div>
      {/each}
      <!-- <div class=" bg-slate-200 w-32 h-20 text-center rounded-lg grid justify-items-center items-center click-motion" on:click={PlusActive = true} style="background-color: hsl(226, 232%, 240% ,0.5) "><img src="plus-solid.svg" alt="북마크 추가하기" class="w-10 h-10"></div> -->
      <!-- <plfavorite/> -->
    </div>
  </div>
</main>
<style>
  .click-motion{
    box-shadow: 0 4px 4px 0 #00000040;
    transition: all 0.3s ease-in-out;
  }
  .click-motion:hover{
    box-shadow: 0 3px 5px rgba(255, 255, 255, 0.2);
        transform: scale(0.97);
        cursor: pointer;
  }
</style>
