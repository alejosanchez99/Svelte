<script>
let count = 1;
$: console.log('count', count); // depends on console and count

$: quadruple = double * 2;

$: double = count * 2; // depends on count
// $: fullName = firstName + '' + lastName; // firstname and lastname
// $: sum = a + b + c; /// a, b, c 
// $: result = calculate(num1, num2); //num1, num2, calculate
// $: doSomething(a,b); //doSomething, a , b

function increment() {
  count ++;
}

function decrement() {
  count --;
}

function doSomething() {
  console.log(double);
}
</script>

<button on:click={decrement}>-</button>
{count} * 2 = {double} * 2 = {quadruple}
<button on:click={increment}>+</button>

<button on:click={doSomething}>Click on me</button>