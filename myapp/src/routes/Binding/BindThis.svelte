<script>
  let element;
  function reset() {
    element.value = "";
  }
</script>

<input bind:this={element} />

<hr />

<button on:click={reset}> reset </button>
