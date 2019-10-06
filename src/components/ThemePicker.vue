<!--
  This is where the list of themes lives! 

  If you're adding a theme, make sure you've also added the theme 
  color variables to ../assets/themes.css 

-->

<!--
  Please add your new theme to the end of the list of themes! 
  
  Properties of <Theme> Components: 

  - theme-name => this is where you'll add the css class to be applied when selected
  - display-name => The name to display on the Theme Picker Element
  - contributor => github username of contributor [If left blank, default github image will be used instead]
  
  Note: The theme-name property on Theme components must be the same as the class name added in themes.css
  If no display-name propery is set, the theme-name will be displayed instead.
--> 

<template>
  <div id="picker">
    <h1>
      Choose a
      <wbr>new theme
    </h1>
    <div class="wrapper">
      <Theme theme-name="default-light" display-name="Default Light" contributor="12vanblart"/>
      <Theme theme-name="default-dark" display-name="Default Dark" contributor="12vanblart"/>
    </div>
    
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
  background-color: var(--accent);
  text-align: center;
  height: 50vh;
  overflow-y: scroll;
  padding: 0 100px;
}

.wrapper {
  display: flex;
  justify-content: center;
}
</style>
