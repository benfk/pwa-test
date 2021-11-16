<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <A2HS/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import A2HS from "@/components/A2HSBtn"

export default {
  name: "Home",
  components: {
    HelloWorld,
    A2HS
  },
};
</script>
