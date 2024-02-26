<script>
  import { tick } from "svelte";

  let count = 1;

  $: double = count * 2; // double -> count

  async function increment() {
    count++;
    console.log("before tick", double);

    await tick();

    console.log("after tick", double);
  }

  function decrement() {
    count--;
  }

  function doSomething() {
    console.log(double);
  }
</script>

<button on:click={decrement}>-</button>
{count} * 2 = {double}
<button on:click={increment}>+</button>

<button on:click={doSomething}>Click on me</button>
