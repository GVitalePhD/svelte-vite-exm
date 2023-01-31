<script>
  import Loader from "./Loader.svelte";

  let show = false;
</script>

<main>
  <h1>Example</h1>
  <p>
    This is the loaded json:
  </p>
  
  <button on:click={ () => show = !show }>
    Show Component</button>
    {#if show}
      <Loader />
    {:else}
      <p> no data!! </p>
    {/if}
</main>

<style>
</style>
