<script>
  import { store2 } from "./data.js";
</script>

<input
  on:input={(e) => {
    $store2 = e.currentTarget.value;
  }}
/>
