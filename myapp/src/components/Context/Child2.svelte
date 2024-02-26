<script>
  import { getContext, setContext } from "svelte";
  import { key } from "./context";
  import GrandChildA from "./GrandChildA.svelte";
  
  const color = getContext(key);
  setContext(key, 'green');
</script>

child2: >> {color}

<GrandChildA />