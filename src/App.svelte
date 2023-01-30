<script>
  let jsonString = 'empty';
  //let fn = 'https://dummyjson.com/docs/products/1';
  //let fn = 'https://jsonplaceholder.typicode.com/';
  let fn = './dummy.json'

  function visJson(filename){
    fetch(filename).then(res => res.json()).then(console.log);
    let promise = fetch(filename).then(res => res.json());
    promise.then((res)=>{
      jsonString = JSON.stringify(res, null, '\n');
    })
  }

  function onClick()
  {
    jsonString = 'waiting...';
    setTimeout(function(){visJson(fn)}, 2000);
  }

</script>

<main>
  <h1>Example</h1>
  <p>
    This is the loaded json:
  </p>
  <p>
    {jsonString}
  </p>
</main>

<button on:click={onClick}>
	Click to load and visualize
</button>

<style>
</style>
