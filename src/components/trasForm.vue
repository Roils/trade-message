<template>
  <div class="tras-form">
    <div class="int-msg">
      <form id="transForm" @submit="formSubmit">
        <el-input type="text" v-model="textToTranslate" style="width:85%" placeholder="输入需要翻译的内容"></el-input>
        <el-select v-model="language" placeholder="请选择">
          <el-option
            v-for="item in options"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          ></el-option>
        </el-select>
        <van-button type="info">翻译</van-button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "tras-head",
  data() {
    return {
      textToTranslate: "",
      language: "",
      options: [
        {
          value: "en",
          label: "中译英"
        },
        {
          value: "ru",
          label: "中译俄"
        },
        {
          value: "ko",
          label: "中译韩"
        },
        {
          value: "ja",
          label: "中译日"
        }
      ]
    };
  },
  methods: {
    formSubmit(e) {
      //alert(this.textToTranslate);
      if(this.textToTranslate == ''){
          return false
      }else{
        this.$emit("formSubmit", this.textToTranslate, this.language);
        e.preventDefault();
      }
    }
  },
  created() {
    this.language = "en";
  }
};
</script>

<style>
.form-lable {
  width: 20%;
  font-size: 0.3rem;
}
.lag-style {
  width: 20%;
  height: 0.4rem;
  outline: none;
}
.int-msg {
  text-align: center;
}
</style>