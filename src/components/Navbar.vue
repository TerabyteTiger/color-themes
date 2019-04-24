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
            <div class="primarySample">--primary: {{ primary }}</div>
            <div class="secondarySample">--secondary: {{ secondary }}</div>
            <div class="accentSample">--accent: {{ accent }}</div>
            <div class="linkSample">--link: {{ link }}</div>
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
export default {
  name: "Navbar",
  components: {
    popper: Popper
  },
  data: function() {
    return {
      primary: "#351c4d",
      secondary: "#fff",
      accent: "#f5ab99",
      link: "#765285"
    };
  },
  methods: {
    updateColors: function() {
      this.primary = getComputedStyle(
        document.querySelector("." + document.getElementById("app").className)
      ).getPropertyValue("--primary");
      this.secondary = getComputedStyle(
        document.querySelector("." + document.getElementById("app").className)
      ).getPropertyValue("--secondary");
      this.accent = getComputedStyle(
        document.querySelector("." + document.getElementById("app").className)
      ).getPropertyValue("--accent");
      this.link = getComputedStyle(
        document.querySelector("." + document.getElementById("app").className)
      ).getPropertyValue("--link");
    }
  },
  mounted() {
    this.$root.$on("themeSelected", () => {
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
  color: var(--primary);
}

.primarySample {
  height: 16pt;
  padding-left: 5px;
  border-left: 15px solid var(--primary);
}

.secondarySample {
  height: 16pt;
  padding-left: 5px;
  border-left: 15px solid var(--secondary);
}

.accentSample {
  height: 16pt;
  padding-left: 5px;
  border-left: 15px solid var(--accent);
}

.linkSample {
  height: 16pt;
  padding-left: 5px;
  border-left: 15px solid var(--link);
}
</style>
