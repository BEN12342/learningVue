<script>
//Define components logic using an object of options such as data, methods and mounted.
//Propeties defined by options are exposed by "this".

export default {
  data() {
    return {
      count: 0,
    };
  },
  //Methods are functions that mutate state and trigger updates
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
      if (this.count < 0) {
        this.count = 0;
      }
    },
  },
  //This will be called when the component is mounted:
  mounted() {},
};
</script>

<template>
  <h1>Options:</h1>
  <button @click="increment">Increment</button>
  <button @click="decrement">Decrement</button>
  <h1>{{ count }}</h1>
</template>