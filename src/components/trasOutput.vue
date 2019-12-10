<template>
  <div class="tras-output">
    <p>{{translatedText}}</p>
  </div>
</template>

<script>
export default {
  name: "tras-output",
  props: ["translatedText"]
};
</script>

<style scoped>
.tras-output {
  width: 94%;
  margin: 0 auto;
  font-size: 0.2rem;
  color: #838B8B;
  margin-top: 0.13rem;
  text-indent: 0.8em;
  word-break: break-all;
  word-wrap: break-word;
}
</style>