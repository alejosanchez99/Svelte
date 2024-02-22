<script>
  let colors = [
    // { name: "red", hex: "#f00" },
    // { name: "green", hex: "#0f0" },
    // { name: "blue", hex: "#00f" },
    // { name: "yellow", hex: "#ff0" },
    // { name: "black" },
  ];

  for (const { name, hex = "purple" } of colors) {
    for (const character of hex) {
      console.log(character);
    }

    console.log(name, hex);
  }

  colors.forEach(({ name, hex = "purple" }, index) => {
    console.log(index);
  });
</script>

<ul>
  {#each colors as { name, hex = 'purple' }, index}
    <li style="color: {hex}">{name} - {index}</li>
    {#each hex as character}
      <li>{character}</li>
    {/each}
  {:else}
    <li>The list is empty</li>
  {/each}
</ul>
