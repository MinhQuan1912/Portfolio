<template>
   <button @click="copy">
      <IconsCopy v-if="!copied" class="text-gray-600 dark:text-gray-dark-600" />
      <IconsChecked v-else class="text-gray-600 dark:text-gray-dark-600" />
   </button>
</template>

<script setup lang="ts">
const props = defineProps<{
   text: string
}>()
const copied = ref(false)
const copy = async () => {
   await navigator.clipboard.writeText(props.text)
   copied.value = true
   setTimeout(() => {
      copied.value = false
   }, 6000)
}
</script>