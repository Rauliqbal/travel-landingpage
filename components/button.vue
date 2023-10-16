<script setup lang="ts">
defineProps<{
  title: string
  icon? : string,
  variant: string,  
}>()
</script>
<template>
  <button :class=" variant + ' inline-flex gap-3 px-8 py-4 font-bold rounded-full items-center'">
    <img v-if="icon?.length" :src="'/img/'+ icon" :alt="title" width="24" height="24">
    {{ title }}
  </button>
</template>