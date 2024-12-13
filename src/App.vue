<script setup lang="ts">
import Currency from "@components/ui/Currency.vue";
import currencies from "@datasets/currencies";
</script>

<template>
  <Currency
    v-for="currency in currencies"
    :key="currency.code"
    :currency="currency"
  />
</template>
