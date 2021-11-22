<template>
  <div>
    <ul>
      <button
        v-for="title in tabsTitles"
        :key="title"
        @click="selectedTitle = title"
      >
        {{ title }}
      </button>
    </ul>
    <slot />
  </div>
</template>

<script>
import { ref, provide } from "vue";
export default {
  setup(props, { slots }) {
    const tabsTitles = ref(slots.default().map((tab) => tab.props.title));
    const selectedTitle = ref(tabsTitles.value[0]);
    provide("selectedTitle", selectedTitle);
    return { tabsTitles, selectedTitle };
  },
};
</script>

<style>
</style>