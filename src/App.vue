<template>
  <div id="app">
    <input v-model="a" />
    <input v-model="b" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  data() {
    return {
      a: 5,
    };
  },
  computed: {
    b: {
      get() {
        return parseInt(this.a) + 1;
      },
      set(v) {
        this.a = v - 1;
      },
    },
  },
  methods: {},
  components: {
    HelloWorld,
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
