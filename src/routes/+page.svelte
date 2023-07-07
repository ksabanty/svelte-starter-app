<script>
  import Nested from "./Nested.svelte";
  let name = "Svelte";
  // let src = "/itysl1.PNG";
</script>

<!-- <img {src} alt="itysl" -->

<h1>Hello, {name.toUpperCase()}!</h1>
<Nested />

<style>
  h1 {
    color: goldenrod;
    font-family: "Comic Sans MS";
  }
</style>
