<template>
  <div class="hello">
    <h2>{{ oneld }}</h2>
    <button>测试</button>
    <input type="text" :value="acs" @input="fn" />
  </div>
</template>

<script>
export default {
  name: "syncTest",
  props: {
    oneld: String,
    title: String,
  },
  data() {
    return { acs: "sad" };
  },
  methods: {
    fn(e) {
      console.log(e.target.value);
      this.$emit("update:title", e.target.value); // 这里单词写错了update也可以a。
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
