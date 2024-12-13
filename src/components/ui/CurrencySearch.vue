<script setup lang="ts">
const search = defineModel("search", {
  type: String,
  required: true,
  default: "",
});
</script>

<template>
  <input
    type="text"
    class="w-full p-2 text-sm outline-none bg-gray-50"
    v-model="search"
    placeholder="Search for a currency"
  />
</template>
