<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <Something msg="Created my own thingy!" />
  <Counter />
  <Options />
  <Composition />
  <Attempt />
  <Another />
  <Event />
</template>

<script>
import SomethingVue from "./components/Something.vue";
import CounterVue from "./components/Counter.vue";
import OptionsVue from "./components/API/Options.vue";
import CompositionVue from "./components/API/Composition.vue";
import AttemptVue from "./components/attempt.vue";
import AnotherVue from "./components/another.vue";
import EventVue from "./components/event.vue"
export default {
  name: "App",
  components: {
    Something: SomethingVue, //Need to remember to do this
    Counter: CounterVue,
    Options: OptionsVue,
    Composition: CompositionVue,
    Attempt: AttemptVue,
    Another: AnotherVue,
    Event: EventVue
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
