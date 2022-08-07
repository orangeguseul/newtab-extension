<script>
  let favorites = ["google", "naver", "cookie"];
</script>

<main>
  <div class="grid">
    <div class="grid grid-cols-4 gap-10 w-96 justify-self-center mt-6">
      {#each favorites as favorite}
        <div class=" bg-orange-300 w-20 h-15 text-center grid justify-items-center">
          <img src="www.{favorite}.com/favicon.ico" alt={favorite} />{favorite}
        </div>
      {/each}
      <div class=" bg-orange-300 w-20 h-15 text-center grid justify-items-center">+</div>
    </div>
  </div>
</main>
