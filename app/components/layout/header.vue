<template>
   <div class="container mx-auto py-4">
      <div class="flex px-8 justify-between ">
         <NuxtLink to="/" class="text-[30px] font-bold leading-[36px] tracking-[-0.02em] text-gray-900 dark:text-gray-dark-900">
            &lt;MQ /&gt;
         </NuxtLink>
         <div class="flex justify-between gap-12 items-center">
            <ul class="flex gap-8 justify-between items-center h-full">
               <li v-for="item in navItems" :key="item" class="h-full text-gray-600 dark:text-gray-dark-600 font-medium transition duration-300 ease-in-out hover:-translate-y-1">
                  <button @click="scrollToSection(item)" class="h-full flex items-center">{{ item }}</button>
               </li>
            </ul>
            <div class="flex justify-between gap-4">
               <UColorModeButton class="w-9 h-9 flex justify-center items-center" />
               <a href="/CV.pdf" download="Nguyen_Minh_Quan_CV.pdf"
                  class="py-1.5 px-4 rounded-xl border-0 bg-gray-900 dark:bg-gray-dark-900 text-gray-50 dark:text-gray-dark-50 font-medium leading-6 
                  hover:text-gray-dark-50 hover:bg-gray-dark-900 dark:hover:text-gray-50 dark:hover:bg-gray-900 transition duration-200 ease-in-out">Download
                  CV
               </a>
            </div>
         </div>
      </div>

   </div>
</template>

<script setup lang="ts">
const navItems = ['About', 'Projects', 'Contact']
function scrollToSection(section: string) {
   const element = document.getElementById(section)
   if (element) {
      element.scrollIntoView({ behavior: 'smooth' })
   }
}
</script>

<style scoped></style>