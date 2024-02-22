<script>
  let count = 0;
  let obj = [];
  
  function increment() {
    // 1. assignment
    // count = 10;
    // 2. update statements
    // count ++;
    // count += 2;
    // 3. updating / assiging a property
    // obj.count++;
    // obj.count = 10;

    // not an update to solve
    const data = obj;
    data.count++;

    obj.push(1);
  }

  function doSomethingElse() {
    obj.foo = 1;
  }
</script>

{JSON.stringify(obj)}

<!-- You can add events -->
<button on:click={increment}>
  Clicked {count}
  {count === 1 ? "time" : "times"}
</button>

<button on:click={doSomethingElse}> Something else </button>