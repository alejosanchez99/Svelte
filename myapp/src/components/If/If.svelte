<script>
  let condition1 = true;
  let condition2 = true;

  function toggleCondition1() {
    condition1 = !condition1;
  }

  function toggleCondition2() {
    condition2 = !condition2;
  }

  function check(condition1, condition2) {
    return condition1 || condition2;
  }
</script>

<button on:click={toggleCondition1}>Condition 1 : {condition1} </button>
<button on:click={toggleCondition2}>Condition 2: {condition2}</button>

{#if condition1 && condition2}
  condition 1 and 2 is true
{:else if check(condition1, condition2)}
  condition 1 or 2 is true
{:else}
  either condition 1 and 2 is false
{/if}
