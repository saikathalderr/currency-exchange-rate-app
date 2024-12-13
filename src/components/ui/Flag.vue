<script setup lang="ts">
import { PropType } from "vue";

const props = defineProps({
  icon: {
    type: String,
    required: true,
  },
  name: {
    type: String,
    required: true,
  },
  size: {
    type: String as PropType<"sm" | "md" | "lg">,
    default: "sm",
  },
});

const flagSizeClass = {
  sm: "w-4 h-4",
  md: "w-8 h-8",
  lg: "w-12 h-12",
};

const flagClass = `rounded-full ${flagSizeClass[props.size]}`;
</script>

<template>
  <img :src="props.icon" :alt="props.name.toLowerCase()" :class="flagClass" />
</template>
