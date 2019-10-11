<template>
  <nav>
    <ul>
      <li>
        <a href="#">
          <h1>Theme Sampler</h1>
        </a>
      </li>
      <li>
        <popper trigger="click" :options="{ placement: 'bottom' }">
          <div class="popper">
            <div class="sample primarySample">--primary: {{ primary }}</div>
            <div class="sample secondarySample">--secondary: {{ secondary }}</div>
            <div class="sample accentSample">--accent: {{ accent }}</div>
            <div class="sample linkSample">--link: {{ link }}</div>
            <div class="sample textSample">--text: {{ text }}</div>
            <hr />
            <div class="floatRight" @click="handleCopyToClipboard">
              <span class="copySample">Copy 📋</span>
            </div>
          </div>
          <a href="#" slot="reference">
            <h1>Hex Codes</h1>
          </a>
        </popper>
      </li>
    </ul>
  </nav>
</template>

<script>
import Popper from "vue-popperjs";
import "vue-popperjs/dist/vue-popper.css";
import copyToClipboard from '../helpers/copyToClipboard.js';

export default {
  name: "Navbar",
  components: {
    popper: Popper
  },
  data: function() {
    return {
      currentTheme: undefined,
      primary: "#351c4d",
      secondary: "#fff",
      accent: "#f5ab99",
      link: "#765285",
      text: "#351c4d"
    };
  },
  methods: {
    updateColors: function() {
      // Grab the variables for the current theme and store them on this component
      this.currentTheme = document.querySelector("." + document.getElementById("app").className);

      this.primary = getComputedStyle(this.currentTheme).getPropertyValue("--primary");
      this.secondary = getComputedStyle(this.currentTheme).getPropertyValue("--secondary");
      this.accent = getComputedStyle(this.currentTheme).getPropertyValue("--accent");
      this.link = getComputedStyle(this.currentTheme).getPropertyValue("--link");
      this.text = getComputedStyle(this.currentTheme).getPropertyValue("--text");
    },

    handleCopyToClipboard: function() {
      if (!this.currentTheme) return

      const { primary, secondary, accent, link, text, currentTheme } = this;
      const theme = `.${currentTheme.getAttribute("class")} {
        --primary: ${primary};
        --secondary: ${secondary};
        --accent: ${accent};
        --link: ${link};
        --text: ${text};
      }`;
      
      copyToClipboard(theme)
    }
  },
  mounted() {
    this.$root.$on("themeSelected", () => {
      // When a new theme is selected, it emits "themeSelected"
      // When this happens, run the .updateColor() function
      this.updateColors();
    });
  }
};
</script>

<style scoped>
nav {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  background-color: var(--primary);
  text-align: left;
  color: var(--secondary);
  padding: 1px 25px;
}

a {
  color: inherit;
  text-decoration: none;
}
h1 {
  width: auto;
  display: block;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
}

li {
  float: left;
}

li a {
  display: block;
  padding: 5px;
}

li:last-child {
  float: right;
}

.popper {
  text-align: left;
  padding: 13px;
  font-size: 17px;
  background-color: var(--secondary);
  color: var(--text);
}

.sample {
  height: 16pt;
  padding-left: 5px;
}

.primarySample {
  border-left: 15px solid var(--primary);
}

.secondarySample {
  border-left: 15px solid var(--secondary);
}

.accentSample {
  border-left: 15px solid var(--accent);
}

.linkSample {
  border-left: 15px solid var(--link);
}

.textSample {
  border-left: 15px solid var(--text);
}

.floatRight {
  float: right;
  cursor: pointer;
}

.copySample:hover {
  text-decoration: underline;
}
</style>
