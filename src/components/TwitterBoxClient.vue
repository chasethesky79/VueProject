<template>
  <div class="input-form">
    <h2>Project Twitter Box Client</h2>
    <form @submit="submitForm" class="ui form">
      <div class="form-input">
        <input
          v-model="newItem"
          type="text"
          placeholder="Enter text!"
          @keydown="onKeyDown"
        />
        <button class="ui button">Submit</button>
      </div>
    </form>
    <div v-if="items.length > 0" class="display-section">
      <ul>
        <li v-for="item in items" :key="item">
          {{ item }},
          <span style="margin-left: 10px"
            >No of characters remaining: {{ 280 - item.length }}</span
          >
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "TwitterBoxClient",
  data() {
    return {
      newItem: "",
      items: [],
    };
  },
  methods: {
    submitForm(event) {
      this.items = [...this.items, this.newItem];
      this.newItem = "";
      event.preventDefault();
    },
    onKeyDown(event) {
      if (this.newItem.length > 280) {
        event.preventDefault();
        return;
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
a {
  color: #42b983;
}
.form-input {
  display: flex;
  justify-content: center;
  margin: 20px 20px 20px 20px;
}
.form-input > * {
  margin: 20px 20px 20px 20px;
}
.form-input input {
  max-width: 500px;
}
form,
.display-section {
  margin: auto;
  width: 50%;
  background-color: aquamarine;
  border: 1px solid;
}
form {
  margin-bottom: 30px;
}
input {
  text-align: center;
}
</style>
