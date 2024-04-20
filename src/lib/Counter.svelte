<script>
  export let initialCount;
  export let maxCount = 10;

  let count = initialCount;
  let string;

  $: {
    string = `You have clicked ${count} times`;
  }

  const increment = () => {
    if (count === maxCount) return;
    count += 1;
  };
</script>

<button class="counter-button" on:click={increment}>
  count is {count}
</button>

<h3>{string}</h3>

<style>
  .counter-button {
    padding: 15px 20px;
    background-color: salmon;
  }
</style>
