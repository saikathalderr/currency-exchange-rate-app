<script setup lang="ts">
import { ref } from "vue";
import CurrencySearch from "@components/ui/CurrencySearch.vue";

const searchText = ref("");
</script>

<template>
  <CurrencySearch v-model:search="searchText" />
</template>
