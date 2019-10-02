<template>
  <div id="picker">
    <h1 class="secondary-text">
      Choose a
      <wbr>new theme
    </h1>
    <Theme v-for="theme in themes" :theme-name="theme.name" :display-name="theme.title" :contributor="theme.contributor"/>
  </div>
</template>

<script>
import Theme from "./Theme.vue";
import data from "@/assets/themes.json";

export default {
  name: "ThemePicker",
  components: {
    Theme
  },
  computed: {
    themes() {
      return data;
    }
  }
};
</script>

<style lang="scss" scoped>
#picker {
  background-color: var(--accent);
  text-align: center;
  height: 50vh;
  overflow-y: scroll;
  padding: 0 100px;
}

.secondary-text {
  background-color: var(--secondary);
}

#picker > button:not(:last-of-type) {
  margin-right: 10px;
}

@media screen and (max-width: 600px) {
  #picker > button:not(:last-of-type) {
    margin-right: 0;
  }
}
</style>
