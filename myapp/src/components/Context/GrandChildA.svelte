<script>
  import { getContext } from "svelte";
  import { key } from "./context";

  const color = getContext(key);
</script>

<div style="color: {color}">GranChild A</div>
