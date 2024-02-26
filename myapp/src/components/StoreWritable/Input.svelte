<script>
  import { valueStore } from "./data.js";
</script>

<input
  on:input={(e) => {
    valueStore.set(e.currentTarget.value);
  }}
/>
