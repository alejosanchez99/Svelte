<script>
  export let name = "Anonymous";
  export let lastName;
  $: fullName = name + " " + lastName;
</script>

<h1>Hello {fullName}!</h1>
