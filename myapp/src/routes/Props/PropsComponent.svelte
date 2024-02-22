<script>
  import PropsExample from "./PropsExample.svelte";

  const obj = {
    name: "Daniel",
    lastName: "Gomez",
  };
</script>

<PropsExample name="Alejandro" lastName="Sanchez" />
<PropsExample {...obj} />
