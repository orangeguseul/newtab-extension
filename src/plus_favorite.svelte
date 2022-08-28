<script>
  export let PlusActive = false;
  let close = () => (PlusActive = false);
</script>
{#if PlusActive}
<main
  class="fixed"
  style="margin-top: -100px;
margin-left: -250px;"
>
  <p>hello</p>
</main>
{/if}
