<script setup lang="ts">
const amount = defineModel("amount", {
  type: Number,
  required: true,
  default: 0,
});
</script>

<template>
  <input
    type="number"
    min="0"
    step="0.01"
    class="text-3xl outline-none font-sans font-bold px-2 py-1"
    v-model="amount"
    autofocus
  />
</template>

<style scoped>
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
input[type="number"] {
  -moz-appearance: textfield;
}
</style>
