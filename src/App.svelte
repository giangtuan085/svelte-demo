<script>
  import Contact from './Contact.svelte';

  export let name;
  export let age = 30;
  let isBold;
  $: uppercaseName = name.toUpperCase(); // label statement
  function incrementAge() {
    age++;
  }

  function changeCss() {
    isBold = !isBold;
  }


</script>

<h1 class={isBold ? 'bold-text' : 'normal-text'}>Hello {uppercaseName}, {age}!</h1>
<button on:click={incrementAge}>Change Age</button>
<button on:click={changeCss}>Change CSS</button>

<input type="text" bind:value={name} />

<Contact name={name}/>
<!-- or just use {name} for short cut -->

<style>
  h1 {
    color: purple;
  }

  .bold-text {
    font-weight: 800;
  }

  .normal-text {
    font-weight: normal;
  }
</style>
