<script>
  // @ts-nocheck

  import Nested from "./Nested.svelte";
  import Arrays from "./Arrays.svelte";
  import PackageInfo from "./PackageInfo.svelte";

  let name = "Svelte";
  // let src = "/itysl1.PNG";
  let count = 0;

  $: if (count >= 10) {
    alert("count is dangerously high");
    count = 0;
  }

  // $ is a label to declare reactive variables
  $: doubled = count * 2;

  function increment() {
    count += 1;
  }

  const pkg = {
    name: "svelte",
    speed: "blazing",
    version: 4,
    website: "https://svelte.dev",
  };
</script>

<!-- <img {src} alt="itysl" -->

<h1>Hello, {name.toUpperCase()}!</h1>
<Nested answer={42} />
<Nested />
<Arrays />
<PackageInfo {...pkg} />

<button on:click={increment}>
  Clicked {count}
  {count === 1 ? "time" : "times"}
</button>

<p>{count} doubled is {doubled}</p>

<style>
  h1 {
    color: goldenrod;
    font-family: "Comic Sans MS";
  }
</style>
