<script>
  let profit = 0;

  $: profitclass = profit < 0 ? "negative" : profit > 0 ? "positive" : "";
  $: negative = profit < 0;
  $: positive = profit > 0;
</script>

<div class={profitclass}>
  {profit}
</div>

<div class:negative class:positive>
  {profit}
</div>

<button
  on:click={() => {
    profit++;
  }}>++</button
>

<button
  on:click={() => {
    profit--;
  }}>--</button
>

<style>
  .negative {
    color: red;
    font-weight: bold;
  }

  .positive {
    color: limegreen;
    font-weight: bold;
  }
</style>
