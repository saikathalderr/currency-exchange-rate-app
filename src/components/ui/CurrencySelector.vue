<script setup lang="ts">
import Flag from "@components/ui/Flag.vue";

const props = defineProps({
  code: {
    type: String,
    required: true,
  },
  icon: {
    type: String,
    required: true,
  },
});

const emit = defineEmits(["click"]);
</script>

<template>
  <div
    class="inline-flex justify-center items-center p-2 cursor-pointer"
    @click="emit('click')"
  >
    <Flag :name="props.code" :icon="props.icon" />
    <span class="text-black font-bold ml-1"> {{ props.code }} </span>
    <img src="@/assets/icons/dropdown.svg" alt="dropdown" />
  </div>
</template>
