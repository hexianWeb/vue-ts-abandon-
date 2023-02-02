<template>
  <hy-input v-model="message"></hy-input>
</template>

<script>
import HyInput from './HyInput.vue';
export default {
  name: 'App',
  components: {
    HyInput,
  },
  data() {
    return {
      message: 'hexianxiane',
    };
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
.active {
  color: red;
}
</style>
