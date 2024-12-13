<script setup lang="ts">
import { defineProps } from "vue";
import Flag from "@components/ui/Flag.vue";
import type { Currency } from "@datasets/currencies";

const props = defineProps({
  currency: {
    type: Object as () => Currency,
    required: true,
  },
});
</script>

<template>
  <button class="w-full text-xs flex gap-2 p-2 hover:bg-gray-100">
    <Flag :name="props.currency.code" :icon="props.currency.flag" />
    <span>
      {{ props.currency.code }}
    </span>
    <span class="text-gray-500">
      {{ props.currency.name }}
    </span>
  </button>
</template>
