<script>
  export let count = 0;
</script>

<button
  on:click={() => {
    count++;
  }}
>
  Increment
</button>

<div>
  Count: {count}
</div>
