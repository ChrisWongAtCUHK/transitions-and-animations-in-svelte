<script>
  import { fade } from 'svelte/transition'
  let showing = false

</script>

<main>
  <label>
    Showing
    <input bind:checked={showing} type="checkbox" />
  </label>
  {#if showing}
    <div transition:fade />
  {/if}
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 4rem;
    padding-block-start: 10rem;
  }

  div {
    height: 200px;
    width: 200px;
    background: goldenrod;
  }
</style>
