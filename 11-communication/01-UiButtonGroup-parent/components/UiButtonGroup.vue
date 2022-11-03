<template>
  <div class="button-group" role="group">
    <!-- Эти кнопки должны передаваться через слот -->
    <button class="button-group__button button-group__button_active" type="button" aria-selected="true">Button1</button>
    <button class="button-group__button" type="button" aria-selected="false">Button2</button>
    <button class="button-group__button" type="button" aria-selected="false">Button3</button>
    <!-- Эти кнопки должны передаваться через слот -->
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
