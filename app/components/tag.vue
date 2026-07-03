<template>
   <p class="rounded-xl border-0 px-5 py-1 bg-gray-200 dark:bg-gray-dark-200 text-gray-600 dark:text-gray-dark-600">
     {{ text }} </p>
</template>

<script setup lang="ts">
defineProps<{
   text: string
}>()
</script>

<style scoped>

</style>