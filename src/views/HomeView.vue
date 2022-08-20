<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" v-model="test" />
    <h1>{{ test }}</h1>
    <syncTest :title.sync="oneld" />
    <h1>{{ oneld }}</h1>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/vModelTest.vue"; // 这个是使用传统的v-model
import syncTest from "@/components/syncTest.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
    syncTest,
  },
  data() {
    return {
      test: "test",
      oneld: "jdisa",
    };
  },
};
</script>
