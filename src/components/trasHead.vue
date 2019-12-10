<template>
  <div id="tras-head">
    <div class="logo">
      <img src="../assets/img/logo.png" />
      <p class="logo-title">智能翻译助手</p>
      <p class="title-msg">一款支持多国语言的在线轻便翻译工具</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "my-head",
  data() {
    return {};
  },
  methods: {}
};
</script>

<style lang="">
.logo {
  width: 100%;
  height: 0.8rem;
  position: relative;
}
.logo img {
  width: 0.5rem;
  height: 0.5rem;
  position: absolute;
  left: 0.1rem;
  top: 0.05rem;
}
.logo-title {
  font-size: 0.17rem;
  display: inline-block;
  position: absolute;
  left: 0.7rem;
  top: 0.23rem;
  color: #1E90FF;
}
.title-msg {
  font-size: 0.13rem;
  position: absolute;
  bottom: 0.1rem;
  left: 0.2rem;
  color: #CDC0B0;
}
</style>