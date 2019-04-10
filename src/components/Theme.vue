<template>
  <div :class="themeName">{{themeName}}</div>
</template>

<script>
export default {
  name: "Theme",
  props: ["themeName"]
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

.primary {
  --primary: #351c4d;
  --secondary: #fff;
  --accent: #f5ab99;
  --link: #765285;
}

.orange {
  --primary: orange;
  --secondary: #fff;
  --accent: #f5ab99;
  --link: #765285;
}
</style>
