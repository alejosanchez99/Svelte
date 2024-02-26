<script>
  import { setContext } from "svelte";
  import { key } from "./context.js";

  import Child2 from "./Child2.svelte";
  import Child from "./Child.svelte";

  setContext(key, "red");
</script>

<div style="border: 1px solid black;">
    Parent A
    <Child2 />
    <Child />
</div>
