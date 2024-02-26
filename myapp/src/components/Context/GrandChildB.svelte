<script>
  import { getContext } from "svelte";
  import { key } from "./context";

  const color = getContext(key);
</script>

<div>GrandChild B: {color}</div>
