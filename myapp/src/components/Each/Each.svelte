<script>
  let colors = [
    { name: "red", hex: "#f00" },
    { name: "green", hex: "#0f0" },
    { name: "blue", hex: "#00f" },
    { name: "yellow", hex: "#ff0" },
    { name: "black" },
  ];

  for (const { name, hex = "purple" } of colors) {
    for (const character of hex) {
      console.log(character);
    }

    console.log(name, hex);
  }
</script>

<ul>
  {#each colors as { name, hex = 'purple' }}
    <li style="color: {hex}">{name}</li>
    {#each hex as character}
      <li>{character}</li>
    {/each}
  {/each}
</ul>
