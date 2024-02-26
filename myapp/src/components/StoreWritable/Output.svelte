<script>
  import { onMount } from "svelte";
  import { valueStore } from "./data";

  let _value;

  onMount(() => {
    return valueStore.subscribe(value=> {      
      _value = value;
    });
  });
</script>

<h1>value: {_value}</h1>
