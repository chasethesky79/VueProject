<template>
  <div class="hello">
    <h1>Starting with directives</h1>
    <h2>{{ name }}</h2>
    <h3>{{ age > 10 ? `Older than 10` : `Younger than 10` }}</h3>
    <a :href="url" target="_blank">Disney</a>
    <h3 v-show="true">Hello</h3>
    <button v-on:click="clicked">Click Me</button>
    <form action>
      <input v-on:keyup.enter="submit" type="`text`" />
      <button v-on:click.prevent="clicked">Submit</button>
      <h3>{{ counter }}</h3>
      <div v-if="counter % 2 === 0">Even</div>
      <div v-else>Odd</div>
      <div v-for="person in people" :key="person.name">
        <h3>{{ person.name }}</h3>
        <span> {{ person.age }}</span>
        <ul>
          <li v-for="value in person" :key="value.name">{{ value }}</li>
        </ul>
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
</style>
