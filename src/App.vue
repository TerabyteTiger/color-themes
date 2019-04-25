<template>
  <div id="app" class="default-light">
    <Navbar/>
    <SelectedTheme/>
    <SampleElements/>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import SampleElements from "./components/SampleElements.vue";
import SelectedTheme from "./components/SelectedTheme.vue";

export default {
  name: "app",
  components: {
    Navbar,
    SampleElements,
    SelectedTheme
  }
};
</script>

<style>
body {
  margin: 0;
  /*Reset Margin of page to 0*/
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--text); /*#2c3e50;*/
  padding-bottom: 150px;
  background-color: var(--secondary);
}

a {
  color: var(--link);
}
</style>

<style src="./assets/themes.css"></style>
