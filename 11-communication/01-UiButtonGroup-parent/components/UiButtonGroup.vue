<template>
  <div class="button-group" role="group">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'UiButtonGroup',

  props: {
    modelValue: {
      required: true,
    },
  },

  emits: ['update:modelValue'],

  expose: ['activeValue', 'updateActiveValue'],

  computed: {
    activeValue() {
      return this.modelValue;
    },
  },

  methods: {
    updateActiveValue(value) {
      this.$emit('update:modelValue', value);
    },
  },
};
</script>

<style scoped>
.button-group {
  display: inline-flex;
  flex-direction: row;
  flex-wrap: wrap;
  white-space: nowrap;
}
</style>
