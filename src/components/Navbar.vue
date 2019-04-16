<template>
  <nav>
    <ul>
      <li>
        <a href="#">
          <h1>Theme Sampler</h1>
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Navbar"
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
  display: inline-block;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

li {
  display: inline;
}
</style>
