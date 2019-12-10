<template>
  <div id="app">
    <tras-head></tras-head>
    <tras-form></tras-form>
    <tras-output></tras-output>
  </div>
</template>

<script>
import trasHead from "./components/trasHead"
import trasForm from "./components/trasForm"
import trasOutput from "./components/trasOutput"
export default {
  name: 'App',
  components: {
    trasForm,
    trasOutput,
    trasHead
  }
}
</script>

<style>

</style>
