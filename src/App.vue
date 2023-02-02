<template>
  <HelloWorld :names="names" v-slot="slotProps">
    <button
      @click="itemClick(slotProps.item)"
      :class="{ active: currentTab === slotProps.item }"
    >
      {{ slotProps.item }}
    </button>
  </HelloWorld>
  <!-- 动态组件 -->
  <!-- 同样支持props参数传递 -->
  <component v-bind:is="currentTab" name="hexian" :age="24"></component>
  <about v-model="message"></about>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import About from './components/About.vue';
import CateGory from './components/CateGory.vue';
import Home from './components/Home.vue';
export default {
  name: 'App',
  components: {
    HelloWorld,
    About,
    CateGory,
    Home,
  },
  data() {
    return {
      names: ['home', 'about', 'category'],
      currentTab: 'home',
      message: 'hexianxiane',
    };
  },
  methods: {
    itemClick(item) {
      this.currentTab = item;
    },
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
