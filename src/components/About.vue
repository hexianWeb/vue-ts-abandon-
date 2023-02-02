<template>
  <h1>组件的V-model</h1>
  <button @click="btnClick">组件传递modelValue</button>
  <h2>{{ modelValue }}</h2>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: 'nobody',
    },
    age: {
      type: Number,
      default: '000',
    },
    modelValue: {
      type: String,
    },
  },
  emits: ['update:modelValue'],
  methods: {
    btnClick() {
      this.$emit('update:modelValue', 'xianhe');
    },
  },
};
</script>

<style></style>
