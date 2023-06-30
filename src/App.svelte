<script>
  import { fade, slide, fly } from 'svelte/transition'
  import { elasticOut } from 'svelte/easing'
  let showing = false

  function custom(node, params) {
    return {
      easing: params.easing,
      css: (t, u) => `transform: translatex(${u * 200}px) scale(${t})`
    }
  }
</script>

<main>
  <label>
    Showing
    <input bind:checked={showing} type="checkbox" />
  </label>
  {#if showing}
    <div transition:custom={{ easing: elasticOut }} />
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
