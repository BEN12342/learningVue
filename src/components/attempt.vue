<script>
export default {
  data() {
    return {
      ok: false,
      number: 20,
      dark: false,
      awesome: false,
    };
  },
  methods: {
    toggle() {
      this.ok = !this.ok;
    },
    toggleMode() {
      const div = document.getElementById("cool");
      if (!this.dark) {
        div.classList.add("dark");
      } else {
        div.classList.remove("dark");
      }
      this.dark = !this.dark;
    },
  },
};
</script>

<template>
  <button @click="toggle">toggle</button>
  <button @click="toggleMode">Toggle colour</button>
  <button @click="awesome = !awesome">Toggle if vue is awesome</button>
  <p v-if="awesome">Vue is awesome!</p>
  <p v-else>Yeah it's not lol</p>
  <div id="cool">
    {{ ok ? "Yes" : "No" }}
  </div>
  <div>
    {{ number + 2 /* Can have any js in here*/ }}
  </div>
  <div>
    {{ date }}
  </div>
  <p v-show="dark">Dark mode is on</p>
</template>

<style scoped>
.cool {
  color: greenyellow;
}

.dark {
  color: red;
}
</style>