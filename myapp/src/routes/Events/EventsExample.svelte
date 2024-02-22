<script>
  import { createEventDispatcher } from "svelte";

  export let name;
  export let status;
  export let onSkillPointChanged = () => {};

  const dispatch = createEventDispatcher();

  let skillPoint = 5;

  // $: onSkillPointChanged(skillPoint);
  $: dispatch("SkillPointChanged", skillPoint);

  function decrementSkillPoint() {
    if (skillPoint > 0) {
      skillPoint--;
    }
  }

  function incrementSkillPoint() {
    skillPoint++;
  }
</script>

<section>
  <dl>
    <dt>Name</dt>
    <dd>{name}</dd>
    <dt>Status</dt>
    <dd>{status}</dd>
  </dl>
</section>

<button on:click={decrementSkillPoint}> - </button>

{skillPoint}

<button on:click={incrementSkillPoint}> + </button>

<style>
  section {
    padding: 10px;
  }
  dd {
    color: rebeccapurple;
  }
</style>
