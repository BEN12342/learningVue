<script>
export default {
  data() {
    return {
      numbers: [1, 2, 3, 4, 5],
    };
  },
  computed: {
    evenNumbers() {
      return this.numbers.filter((n) => n % 2 === 1);
    },
  },
};
</script>

<template>
  <li v-for="n in evenNumbers" :key="n">{{ n }}</li>
</template>