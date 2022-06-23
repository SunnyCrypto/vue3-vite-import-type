<template>
  <button :class="[`e-button--${theme}`]">
    <slot></slot>
  </button>
</template>

<script setup lang="ts">
import type { ButtonProps } from './Button.type'
const props = withDefaults(defineProps<ButtonProps>(), {
  theme: 'primary'
})
</script>

<style>
.e-button--primary {
  padding: 0.6em 1.2em;
  color: #fff;
  background-color: #1199fa;
  border-radius: 4px;
  border: 0;
  outline: none;
}
</style>