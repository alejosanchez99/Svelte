<script>
  import { fade } from "svelte/transition";

  let count = 0;
</script>

{#key count}
  <input in:fade />
  <div in:fade>
    {count}
  </div>
{/key}

<button on:click={() => count++}>
  {count}
</button>
