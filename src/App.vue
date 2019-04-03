<template>
  <div id="app" class="main">
    <Navbar/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <SampleElements/>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import SampleElements from "./components/SampleElements.vue";

export default {
  name: "app",
  components: {
    Navbar,
    SampleElements
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  border: 0;
  outline: 0;
  vertical-align: baseline;
  background: transparent;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.main {
  --primary: #351c4d;
  --secondary: #fff;
  --accent: #f5ab99;
  --link: #765285;
}
</style>
