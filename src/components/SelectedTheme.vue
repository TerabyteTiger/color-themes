<template>
  <div>
    <button id="selected-Theme" @click="themePicker()" class="no-select">
      <h1 class="btn">Click to change theme</h1>
    </button>
    <transition name="expand">
      <ThemePicker v-show="showPicker"/>
    </transition>
  </div>
</template>

<script>
import ThemePicker from "./ThemePicker.vue";

export default {
  name: "SelectedTheme",
  data: function() {
    return {
      showPicker: false
    };
  },
  components: {
    ThemePicker
  },
  methods: {
    themePicker() {
      this.showPicker = !this.showPicker;
    }
  }
};
</script>


<style lang="scss" scoped>
#selected-Theme {
  background-color: var(--secondary);
  border: 5px solid var(--primary);
  color: var(--accent);
  box-shadow: 0 0 4px #333;
  border-radius: 17px;
  min-height: 50px;
  width: 50%;
  margin: 10px auto auto;
  padding: 10px;
  text-align: center;
}

.btn:hover {
  text-decoration: underline;
}

.no-select {
  -webkit-touch-callout: none; /* iOS Safari */
  -webkit-user-select: none; /* Safari */
  -khtml-user-select: none; /* Konqueror HTML */
  -moz-user-select: none; /* Firefox */
  -ms-user-select: none; /* Internet Explorer/Edge */
  user-select: none; /* Non-prefixed version, currently supported by Chrome and Opera */
}

.expand-enter-active {
  animation: expand-in 1.5s;
}

.expand-leave-active {
  animation: expand-in 1.5s reverse;
}

@keyframes expand-in {
  0% {
    height: 0;
  }
  100% {
    height: 50vh;
  }
}

div {
  text-align: center;
}
</style>
