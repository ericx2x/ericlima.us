<template>
  <div class="home">
    <Robot />
    <img alt="Vue logo" src="../assets/developer-background.jpg" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Robot from "@/components/Robot.vue";

export default {
  name: "home",
  components: {
    HelloWorld,
    Robot
  }
};
</script>

<style>
.home{
  /* background: red; */
}
</style>