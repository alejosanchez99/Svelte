<script>
  import OnMountExample1 from "./OnMountExample1.svelte";
  import OnMountExample2 from "./OnMountExample2.svelte";

  let show = false;
</script>

<input bind:checked={show} type="checkbox" />

{#if show}
  <OnMountExample1 />
  <OnMountExample2 />
{/if}
