<template>
  <div class="samples">
    <div class="card">
      <h1>A11y</h1>
      <div class="primary-ally">
        <p class="small black">This is what dark text on your primary color looks like</p>
        <p class="large black">This is what large dark text on your primary color looks like</p>
        <p class="small white">This is what white text on your primary color looks like</p>
        <p class="large white">This is what large white text on your primary color looks like</p>
      </div>
      <hr>
      <div class="secondary-ally">
        <p class="small black">This is what dark text on your secondary color looks like</p>
        <p class="large black">This is what large dark text on your secondary color looks like</p>
        <p class="small white">This is what white text on your secondary color looks like</p>
        <p class="large white">This is what large white text on your secondary color looks like</p>
      </div>
    </div>

    <div class="card">
      <h1>Headers</h1>
      <h1 class="left">This is an h1 tag</h1>
      <h2>This is an h2 tag</h2>
      <h3>This is an h3 tag</h3>
      <h4>This is an h4 tag</h4>
    </div>

    <div class="card center">
      <h1>Tables</h1>
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

    <div class="card">
      <h1>Paragraphs</h1>
      <p>This is a sample paragraph. It has one line.</p>
      <p>
        This is also a sample paragraph, but it has more content! There's a sentence
        about dogs. There's a sentence about cats. There's a sentence about birds. There's
        a sentence about fish. There's a sentence about pigs. There's a sentence about
        cows. There's even one about bears!
      </p>
    </div>

    <div class="card">
      <h1>Lists</h1>
      <h2>Unordered Lists</h2>
      <h3>Things I like</h3>
      <ul>
        <li>Themes</li>
        <li>Code</li>
        <li>Coffee</li>
      </ul>

      <h2>Ordered Lists</h2>
      <h3>My Favorite Colors</h3>
      <ol>
        <li>Yellow</li>
        <li>Purple</li>
        <li>Aqua</li>
      </ol>
    </div>

    <div class="card center">
      <h1>Images</h1>
      <img
        src="http://placekitten.com/200/300"
        alt="200 by 300 random cat picture from Placekitten"
      >
    </div>

    <div class="card center">
      <h1>Forms (Inputs)</h1>
      <form>
        <label for="fname">First Name</label>
        <input type="text" id="fname" name="firstname" placeholder="Your name..">
        <br>
        <label for="lname">Last Name</label>
        <input type="text" id="lname" name="lastname" placeholder="Your last name..">
        <br>
        <label for="country">Country</label>
        <select id="country" name="country">
          <option value="australia">Australia</option>
          <option value="canada">Canada</option>
          <option value="usa">USA</option>
        </select>
        <br>
        <label for="subject">Subject</label>
        <textarea id="subject" name="subject" placeholder="Write something.." style="height:200px"></textarea>
        <br>
        <input type="submit" value="Submit">
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "SampleElements"
};
</script>

<style lang="scss" scoped>
/*General classes*/
.center {
  text-align: center;
}

.left {
  text-align: left;
}

.large {
  font-size: 14pt;
  font-weight: bold;
}

.small {
  font-size: 12pt;
}

.white {
  color: white;
}

.black {
  color: #333333;
}

/* Material Card setup */
.card {
  color: var(--primary);
  background-color: var(--secondary);
  border: 3px solid var(--accent);
  width: 50%;
  margin: 10px auto auto;
  border-radius: 17px;
  padding: 10px;
  box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14),
    0 3px 1px -2px rgba(0, 0, 0, 0.12), 0 1px 5px 0 rgba(0, 0, 0, 0.2);

  > h1:nth-child(1) {
    text-align: center;
  }
}

/* A11y Section */
.primary-ally {
  background-color: var(--primary);
}

.secondary-ally {
  background-color: var(--secondary);
}

/* Table Styling */
table {
  width: 100%;
  border-collapse: collapse;
}

tr:nth-child(even) {
  background-color: gainsboro;
}
</style>
