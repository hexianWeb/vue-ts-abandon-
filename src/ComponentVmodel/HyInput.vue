<template>
  <input type="text" v-model="value" />
  <h2>{{ modelValue }}</h2>
</template>

<script>
export default {
  props: {
    modelValue: String,
  },
  emits: ['update:modelValue'],
  computed: {
    value: {
      set(value) {
        this.$emit('update:modelValue', value);
      },
      get() {
        return this.modelValue;
      },
    },
  },
};
</script>

<style></style>
