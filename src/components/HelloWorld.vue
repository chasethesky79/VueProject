<template>
  <div class="input-form">
    <h2 class="ui header">Project Twitter Box Client</h2>
    <form class="ui form">
      <div class="form-input">
        <input ref="newItem" type="text" placeholder="Add an item!" />
        <button class="ui button">Submit</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      name: `This is hello`,
      age: 35,
      url: "https://www.disney.com",
      info: `<div><h1>From Date</h1></div`,
      counter: 0,
      people: [
        { name: "Bharath", age: 20 },
        { name: "Jill", age: 25 },
        { name: "John", age: 27 },
      ],
    };
  },
  methods: {
    clicked(event) {
      console.log(`CLICKED ${event.target.value}`);
      this.counter++;
    },
    submit() {
      alert("Enter");
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
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.form-input {
  display: flex;
  justify-content: center;
}
.form-input > * {
  margin: 20px 20px 20px 20px;
}
.form-input input {
  max-width: 500px;
}
.form-input {
  margin: 20px 20px 20px 20px;
}
form {
  margin: auto;
  width: 50%;
  background-color: aquamarine;
  border: 1px solid;
}
</style>
