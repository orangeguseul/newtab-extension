<script>
  let favorites = [{name:'google',url:'www.google.com'}, {name:'naver',url:'www.naver.com'}, {name:'youtube',url:'www.youtube.com'}];
</script>

<main>
  <div class="grid">
    <div class="grid grid-cols-4 gap-3.5 w-4/12 justify-self-center mt-6">
      {#each favorites as favorite}
        <div class="bg-slate-200 w-32 h-20 text-center grid justify-items-center rounded-lg" style="background-color: hsl(226, 232%, 240% ,0.5) ">
          <a href="https://{favorite.url}" style="opacity: 1">
            <img src="https://{favorite.url}/favicon.ico" alt="{favorite.name}" class="w-10 h-10 justify-self-center mr-10 ml-10" style="opacity: 1"/>{favorite.name}
          </a>
        </div>
      {/each}
      <div class=" bg-slate-200 w-32 h-20 text-center rounded-lg grid justify-items-center items-center" style="background-color: hsl(226, 232%, 240% ,0.5) "><img src="plus-solid.svg" alt="북마크 추가하기" class="w-10 h-10"></div>
    </div>
  </div>
</main>
