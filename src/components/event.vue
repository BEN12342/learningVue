<script>
export default {
  data() {
    return {
      name: "Ben",
    };
  },
  methods: {
    greet(event) {
      alert(`hello ${this.name}!`);

      if (event) {
        alert(`${event.target.tagName}`);
      }
    },
    say(message) {
      alert(message);
    },
    warn(message, event) {
      if (event) {
        event.preventDefault();
      }
      alert(message);
    },
  },
};
</script>

<template>
  <button @click="greet">Click</button>
  <button @click="say('hello')">Say hello</button>
  <button @click="(event) => warn('Form Cant be submitted', event)">
    Click
  </button>
</template>