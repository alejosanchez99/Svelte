<script>
  import { setContext } from "svelte";
  import GrandChildA from "./GrandChildA.svelte";
  import { key } from "./context";

  setContext(key, "blue");

</script>

<GrandChildA />
