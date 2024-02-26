<script>
    import { onMount, onDestroy, afterUpdate, beforeUpdate } from "svelte";
  
    let count = 0;
  
    onMount(() => {
      console.log("onMount");
    });
  
    onDestroy(() => {
      console.log("onDestroy");
    });
  
    beforeUpdate(() => {
      console.log('beforeUpdate');
    });
  
    afterUpdate(() => {
      console.log('afterUpdate');
    })
  
    function update(params) {
      count++;
    }
  </script>
  
  
  <button on:click={update}>Click me</button>
  
  {count}
  