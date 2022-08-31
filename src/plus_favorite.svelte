<script>
  import { writable } from 'svelte/store'
  export const PlusActive = writable(false);
  let close = () => (PlusActive.set(true));
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
