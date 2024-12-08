<script setup lang="ts">
import Amount from "@components/ui/Amount.vue";
import { ref } from "vue";

const amount = ref(0);
</script>

<template>
  <h2>
    {{ amount }}
  </h2>
  <Amount v-model:amount="amount" />
</template>
