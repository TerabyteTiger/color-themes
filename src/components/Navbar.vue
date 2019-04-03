<template>
  <div>
    <a href="#">
      <h1>Tyler's Theme Sampler</h1>
    </a>
  </div>
</template>

<script>
export default {
  name: "Navbar"
};
</script>

<style scoped>
div {
  position: sticky;
  background-color: var(--primary);
  text-align: left;
  color: var(--secondary);
  padding: 7px 25px;
}

a {
  color: inherit;
  text-decoration: none;
}
</style>
