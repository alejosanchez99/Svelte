<script>
  import EventsExample from "./EventsExample.svelte";

  function onSkillPointChanged(newSkillPoint) {
    console.log("onSkillPointChanged", newSkillPoint);
  }

  function onSkillPointChanged2(event) {
    console.log("onSkillPointChanged", event.detail);
  }
</script>

<EventsExample
  name="Alejandro"
  status="Learning Svelte"
  {onSkillPointChanged}
/>

<EventsExample
  name="Alejandro"
  status="Learning Svelte"
  on:SkillPointChanged={onSkillPointChanged2}
/>
