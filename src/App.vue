<template>
  <div class="container">
    <Sidebar />
    <MainSection />
  </div>
  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
</template>

<script>
import MainSection from "./components/MainSection.vue";
// import HelloWorld from "./components/HelloWorld.vue";
import Sidebar from "./components/Sidebar.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    Sidebar,
    MainSection,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Georama:wght@300;400;500;600;900&display=swap");
.container {
  font-family: Georama;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  display: grid;
  grid-template-columns: 0.1fr 4fr;
}
</style>
