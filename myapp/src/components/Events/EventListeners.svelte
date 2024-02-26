<script>
  function onClick() {
    console.log("clicked");
  }

  // h1.addEventListener('click', onClick)
</script>

<h1 on:click|preventDefault|stopPropagation={onClick}>Event listeners</h1>

<div
  on:click={() => {
    console.log("Parent");
  }}
>
  Parent
  <div
    on:click|stopPropagation={() => {
      console.log("child");
    }}
  >
    Child
  </div>
</div>
