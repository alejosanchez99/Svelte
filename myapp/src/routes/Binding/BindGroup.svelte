<script>
  let flavours = [];
  let option = "3";
  let options = ["3"];
</script>

<label for="">
  <input type="checkbox" bind:group={flavours} value="1" /> 1
</label>

<label for="">
  <input type="checkbox" bind:group={flavours} value="2" /> 2
</label>

<label for="">
  <input type="checkbox" bind:group={flavours} value="3" /> 3
</label>

<div>
  Flavours: {flavours.join(",") || "-"}
</div>

<button
  on:click={() => {
    option = "3";
  }}
>
  Reset
</button>

<label for="">
  <input type="radio" bind:group={option} value="1" /> 1
</label>

<label for="">
  <input type="radio" bind:group={option} value="2" /> 2
</label>

<label for="">
  <input type="radio" bind:group={option} value="3" /> 3
</label>

<div>
  Selected option: {option || "-"}
</div>

<label for="">
    <input type="checkbox" bind:group={options} value="1" /> 1
  </label>
  
  <label for="">
    <input type="checkbox" bind:group={options} value="2" /> 2
  </label>
  
  <label for="">
    <input type="checkbox" bind:group={options} value="3" /> 3
  </label>
  
  <div>
    Selected options: {options.join(',' ) || "-"}
  </div>