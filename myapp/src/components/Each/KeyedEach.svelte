<script>
  import KeyedEachComponent from "./KeyedEachComponent.svelte";


  let colors = ["red", "green", "blue"];

  function addColors() {
    colors.splice(2, 0, "yellow");
    colors = colors;
  }
</script>

<button on:click={addColors}> click </button>

<ul>
  {#each colors as color (color)}
    <li>
      {color} (key:{color})
    </li>
    <KeyedEachComponent {color} />
  {/each}
</ul>
