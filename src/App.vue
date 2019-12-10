<template>
  <div id="app">
    <tras-head></tras-head>
    <tras-form v-on:formSubmit="translateText"></tras-form>
    <tras-output v-text="translatedText"></tras-output>
  </div>
</template>

<script>
import trasHead from "./components/trasHead";
import trasForm from "./components/trasForm";
import trasOutput from "./components/trasOutput";
export default {
  name: "App",
  data() {
    return {
      translatedText: '',
      loading: true
    };
  },
  components: {
    trasForm,
    trasOutput,
    trasHead
  },
  methods: {
    translateText(text, language) {
      this.$http
        .get(
          "https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20190624T033609Z.879dfee5391e4e2c.64c6b2ca15bf961de69b7c053199a60b0e82e0d9&lang=" +
            language +
            "&text=" +
            text
        )
        .then(response => {
          //console.log(response.body.text[0]);
          this.translatedText = response.body.text[0];
        });
    }
  }
};
</script>

<style>
</style>
