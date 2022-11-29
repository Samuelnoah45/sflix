<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  classStyle: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div
    :class="classStyle"
    class="flex justify-center items-center p-4 hover:cursor-pointer rounded-lg space-x-3 hover:scale-110  shadow-[100px,100px,100px.100px]   duration-300 hover:shadow-secondary"
  >
    <span>{{ title }}</span>
    <slot></slot>
  </div>
</template>
