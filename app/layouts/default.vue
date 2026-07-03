<template>
   <div class="relative">
      <div class="fixed left-0 right-0 z-3 w-full bg-white dark:bg-[#0f172b]">
         <LayoutHeader />
      </div>
      <slot />
      <button :class="[
         'hidden md:flex fixed bottom-8 right-15 w-11.5 h-11.5 justify-center items-center rounded-full bg-gray-700 z-5 text-gray-50 hover:text-gray-900 hover:bg-gray-200 transition-all duration-500',
         scrollY > 400
            ? 'opacity-100 '
            : 'opacity-0  pointer-events-none'
      ]" @click="y -= y">
         <IconsArrow2 class="-rotate-90 cursor-pointer" />
      </button>
      <LayoutFooter />
   </div>

</template>

<script setup lang="ts">
const { y } = useWindowScroll({ behavior: 'smooth' });
const scrollY = computed(() => y.value)
</script>

<style scoped></style>