<script>
  import BindingComponent from "./BindingComponent.svelte";

  let value = "";
  let count = 0;

  function onInput(event) {
    value = this.value;
  }
</script>

<!-- Both of them are the same -->
<input on:input={onInput} {value} type="text" />
<input bind:value type="text" />
<input bind:value type="text" />
<!-- In this case if the bind value has the same name, you can use that -->

<button on:click={() => (value = "asas")}> Click me </button>

<div>
  Value: "{value}"
</div>

<BindingComponent bind:count />

<button
  on:click={() => {
    count = 999;
  }}
>
  Click me
</button>
