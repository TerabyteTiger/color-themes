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
    <h1 class="secondary-text">
      Choose a
      <wbr>new theme
    </h1>
    <div class="wrapper">
      <Theme theme-name="default-light" display-name="Default Light" contributor="12vanblart"/>
      <Theme theme-name="default-dark" display-name="Default Dark" contributor="12vanblart"/>
      <Theme theme-name="roseGold" display-name="Rose Gold" contributor="stroudn1"/>
      <Theme theme-name="fish-finger" display-name="Fishfinger" contributor="iamjinme"/>
      <Theme theme-name="forest-theme" display-name="Forest Theme" contributor="ewenearle"/>
      <Theme theme-name="arduino-theme" display-name="Arduino Theme" contributor="babel78"/>
      <Theme theme-name="morning-blue" display-name="Morning Blue" contributor="chinmay81098"/>
      <Theme theme-name="bubblegum" display-name="Bubblegum" contributor="heatherpekrul"/>
      <Theme theme-name="dracula" display-name="Dracula" contributor="SpaceLenore"/>
      <Theme theme-name="purple-haze" display-name="Purple Haze" contributor="CariZa"/>
      <Theme theme-name="planet-express" display-name="Planet Express" contributor="kylerits" />
      <Theme theme-name="coder" display-name="Coder Theme" contributor="ashishohri"/>
      <Theme theme-name="soft-haze" display-name="Soft Haze Theme" contributor="rebz"/>
      <Theme theme-name="light-dark" display-name="Light Dark" contributor="natandias"/>
      <Theme theme-name="gameboy" display-name="Gameboy" contributor="morsecodemedia"/>
      <Theme theme-name="dark-blue" display-name="Blue" contributor="max003003003"/>
      <Theme theme-name="blue-theme" display-name="Blue Theme" contributor="lupecio"/>
      <Theme theme-name="capuccino" display-name="Capuccino" contributor="alexandrehiroyuki"/>
      <Theme theme-name="panda-theme" display-name="Panda Theme" contributor="gustavomagalhaes"/>
      <Theme theme-name="simple-blue" display-name="Simple Blue Theme" contributor="abdulamite"/>
      <Theme theme-name="primarily-pink" display-name="Primarily Pink" contributor="karaluton"/>
      <Theme theme-name="a-purple-theme" display-name="A Purple Theme" contributor="jonathanfsilva" />
      <Theme theme-name="material-green" display-name="Material Green" contributor="Lucas-FilipeSS"/>
      <Theme theme-name="classic-retro" display-name="Classic Retro" contributor="prismprince" />
      <Theme theme-name="vintage-warm" display-name="Vintage Warm" contributor="prismprince" />
      <Theme theme-name="october-orange" display-name="October orange" contributor="CNname" />
      <Theme theme-name="red-theme" display-name="Red Theme" contributor="iamshadmirza" />
      <Theme theme-name="black-yellow" display-name="Black yellow" contributor="pipitorminator"/>
      <Theme theme-name="sunset-blue" display-name="Sunset blue" contributor="mannuelf" />
      <Theme theme-name="maybe-brown" display-name="Maybe brown" contributor="saurabhsabharwal"/>
      <Theme theme-name="skyblue-theme" display-name="skyblue-theme" contributor="LRK1696"/>
      <Theme theme-name="ninja-theme" display-name="Ninja Theme" contributor="shekhar677"/>
      <Theme theme-name="soft-theme" display-name="Soft Theme" contributor="eduardosgs"/>
      <Theme theme-name="pink-black" display-name="Pink Black" contributor="tummala-manasa"/>
      <Theme theme-name="pcc-theme" display-name="PCC Theme" contributor="paulo-filho-dev"/>
      <Theme theme-name="brazil" display-name="Brazil" contributor="matheusuehara"/>
      <Theme theme-name="nord" display-name="Nord" contributor="jomagus"/>
      <Theme theme-name="starling-purple" display-name="Starling Purple" contributor="rahuldkjain"/>
      <Theme theme-name="fatec-theme" display-name="Fatec Theme" contributor="felipez3r0"/>
      <Theme theme-name="violet-theme" display-name="Violet Theme" contributor="RedFaction"/>
      <Theme theme-name="discord-theme" display-name="Discord Theme" contributor="FlouksBerlin"/>
      <Theme theme-name="minty-theme" display-name="Minty Theme" contributor="sharadasowmya14"/>
      <Theme theme-name="hacker-theme" display-name="hacker-theme" contributor="bartektelec"/>
      <Theme theme-name="black-olive-theme" display-name="Black Olive Theme" contributor="kotanagasruthi"/>
      <Theme theme-name="vlad4him-theme" display-name="Vlad4him Theme" contributor="vlad4him"/>
      <Theme theme-name="ayu-theme" display-name="Ayu Theme" contributor="tatthien"/>
      <Theme theme-name="selesnya" display-name="Selesnya" contributor="Joseph-Whiunui"/>
      <Theme theme-name="red-brown" display-name="Red brown" contributor="Topekz"/>
      <Theme theme-name="white-darkblack" display-name="White black" contributor="narayanashanubhog"/>    
      <Theme theme-name="nature-theme" display-name="Nature Theme" contributor="sivanbecker"/>
      <Theme theme-name="mint-forest" display-name="Mint Forest" contributor="ydegtyar"/>
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

.wrapper {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
</style>
