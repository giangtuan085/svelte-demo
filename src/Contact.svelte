<script>
  export let name;
  $: uppercaseName = name.toUpperCase(); // label statement

</script>

<div class="container">
    <header>
        <h1>User:</h1><h2>{name}</h2>
        <h2>Job Title</h2>
    </header>
</div>

<style>
  h1 {
    color: grey;
  }
</style>
