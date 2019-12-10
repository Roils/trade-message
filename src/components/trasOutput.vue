<template>
    <div class="tras-output">
        <p class="out-p">{{translatedText}}</p>
    </div>
</template>

<script>
export default {
  name: 'tras-output',
  props:["translatedText"]
}
</script>

<style scoped>
.tras-output{
    width: 100%;
    font-size: .3rem;
    text-align: center;
    color: #363636;
    margin-top: .13rem;
}
</style>