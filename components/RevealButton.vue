<script setup lang="ts">
defineProps<{
  catName: string;
}>();

const revealed = ref(false);
</script>

<template>
  <button
    v-if="!revealed"
    class="bg-white border py-1 px-2 rounded-md text-black"
    @mousedown="revealed = true"
    ref="button"
  >
    Button
  </button>
  <div v-else class="text-4xl font-bold">{{ catName }}</div>
</template>
