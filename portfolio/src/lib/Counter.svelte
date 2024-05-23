<script>
  let count = 0
  $: cuenta = count + 4
  const increment = () => {
    count += 1
  }
</script>

<button on:click={increment}>
  count is {count}
</button>

{cuenta}
