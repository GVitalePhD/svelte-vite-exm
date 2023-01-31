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
      <!-- <p> {visJson()} </p>  
      <p> {jsonString} </p> -->
      <Loader />
    {:else}
      <p> no data!! </p>
    {/if}
</main>

<!-- <button on:click={onClick}>
	Click to load and visualize
</button>
function onClick()
      {
        jsonString = 'waiting...';
        setTimeout(visJson, 2000);
      }
 -->

<style>
</style>
