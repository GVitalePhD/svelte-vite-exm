<script>
    import {onMount, onDestroy} from 'svelte'
    
      let jsonString = 'empty';
      let promise;
      //let fn = 'https://dummyjson.com/docs/products/1';
      //let fn = 'https://jsonplaceholder.typicode.com/';
      const filename = './dummy.json'
    
      onMount(async () => {
        console.log('activating the loader');
        promise = fetch(filename)
            .then(res => res.json())
            .then((res)=>{jsonString = JSON.stringify(res, null, '\n');})
        });
      
      onDestroy(() => {console.log('closing the loader');});
</script>
    
<p> {jsonString} </p>