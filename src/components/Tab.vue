<template>
  <div v-show="title === selectedTitle">
    <slot />
    <h1>{{ show }}</h1>
  </div>
</template>

<script>
import {  defineComponent, inject } from "vue";
export default defineComponent({
  props:['title'],
    setup() {
      const selectedTitle = inject("selectedTitle");
      return { selectedTitle };
    },
  });
</script>

<style>
</style>