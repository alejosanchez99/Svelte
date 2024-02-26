<script>
  import LifecycleExample from "./LifecycleExample.svelte";

  let condition;
</script>

<input type="checkbox" bind:checked={condition} />

{#if condition}
  <LifecycleExample />
{/if}
