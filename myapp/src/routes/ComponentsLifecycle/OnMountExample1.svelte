<script>
  import { onDestroy, onMount } from "svelte";

  let count = 0;
  let intervalId;

  onMount(() => {
    intervalId = setInterval(() => {
      console.log("count", ++count);
    }, 1000);

    return () => {
      clearInterval(intervalId);
    };
  });
</script>

{count}
