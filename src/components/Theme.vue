<template>
  <div :class="themeName" @click="setTheme">{{themeName}}</div>
</template>

<script>
export default {
  name: "Theme",
  props: ["themeName"],
  methods: {
    setTheme() {
      document.getElementById("app").className = this.themeName;
      this.$root.$emit("themeSelected");
    }
  }
};
</script>

<style scoped>
div {
  float: left;
  width: 150px;
  padding: 35px 0;
  overflow: hidden;
  margin-left: 10px;
  border-radius: 5px;
  border: 5px solid var(--primary);
  background-color: var(--secondary);
  color: var(--primary);
}
</style>

<style scoped src="../assets/themes.css">
</style>
