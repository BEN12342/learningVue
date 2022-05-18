<template>
  <div class="something">
    <h1>Hello</h1>
    <h2>{{ msg }}</h2>
    <p>Using text interpolation: {{ rawHtml }}</p>
    <p>Using v-html directive: <span v-html="rawHtml"></span></p>
  </div>
</template>

<script>
export default {
  name: "something",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
.something {
  color: green;
}
</style>