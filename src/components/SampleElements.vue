<template>
  <div class="samples">
    <div>
      <h1>This is an h1 tag</h1>
      <h2>This is an h2 tag</h2>
      <h3>This is an h3 tag</h3>
      <h4>This is an h4 tag</h4>
    </div>

    <table>
      <thead>
        <tr>
          <th>Username</th>
          <th>Age</th>
          <th>Style</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>jsmith</td>
          <td>32</td>
          <td>Primary</td>
        </tr>

        <tr>
          <td>jsmith</td>
          <td>32</td>
          <td>Secondary</td>
        </tr>

        <tr>
          <td>jsmith</td>
          <td>32</td>
          <td>Tertiary</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "SampleElements"
};
</script>

<style scoped>
table {
  width: 100%;
}

.card {
  color: var(--primary);
  background-color: var(--secondary);
  border: 3px solid var(--accent);
  width: 50%;
  margin: auto;
  border-radius: 17px;
}
</style>
