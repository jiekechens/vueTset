<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{ test }}</h2>
    <button>测试v-modela</button>
    <input type="text" :value="title" @input="fn" />
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
    test: String,
  },
  model: {
    prop: "test",
    event: "test",
  },
  data() {
    return { title: "sad" };
  },
  methods: {
    fn(e) {
      console.log(e.target.value);
      this.$emit("test", e.target.value);
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
