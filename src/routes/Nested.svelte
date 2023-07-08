<script>
  let string = `this string contains some <strong>HTML</strong>`;
  export let answer = "a mystery";
</script>

<!-- <p>{@html string}</p> -->
<p>The answer is {answer}</p>

<style>
  p {
    color: blue;
    font-family: "Comic Sans MS";
  }
</style>
