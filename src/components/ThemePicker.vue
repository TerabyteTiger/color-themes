<template>
  <div id="picker">
    <h1>Choose a new theme</h1>
    <Theme theme-name="primary"/>
    <Theme theme-name="dark"/>
  </div>
</template>

<script>
import Theme from "./Theme.vue";
export default {
  name: "ThemePicker",
  components: {
    Theme
  }
};
</script>

<style lang="scss" scoped>
#picker {
  background-color: gainsboro;
  text-align: center;
  height: 50vh;
  overflow-y: scroll;
}
</style>

