<template>
  <button :class="themeName" @click="setTheme">
    {{ displayName ? displayName : themeName }}
    <br>
    <img class="gitProf" :src="githubProfile">
  </button>
</template>

<script>
export default {
  name: "Theme",
  props: ["themeName", "displayName", "contributor"],
  methods: {
    setTheme() {
      // Update the app to use the selected theme & emit "themeSelected" to trigger other component functions
      document.getElementById("app").className = this.themeName;
      this.$root.$emit("themeSelected");
    }
  },
  computed: {
    githubProfile: function() {
      return "https://www.github.com/" + this.contributor + ".png";
    }
  }
};
</script>

<style scoped>
button {
  float: left;
  width: 150px;
  padding: 35px 0;
  overflow: hidden;
  margin-left: 10px;
  margin-top: 10px;
  border-radius: 5px;
  border: 5px solid var(--primary);
  background-color: var(--secondary);
  color: var(--primary);
}

@media screen and (max-width: 600px) {
  button {
    width: 100%;
  }
}

.gitProf {
  width: 50px;
  border-radius: 10px;
  margin-top: 5px;
}
</style>

<style scoped src="../assets/themes.css">
</style>
