<template>
   <div id="About" class="container mx-auto">
      <div class="flex gap-12 justify-between px-8 py-24">
         <div class="flex flex-col gap-12 justify-between">
            <div class="flex flex-col gap-2 justify-between">
               <h1 class="text-6xl font-bold leading-18 tracking-[-0.02em] text-gray-900 dark:text-gray-dark-900">Hi,
                  I'm
                  Quan👋</h1>
               <p class="leading-6 text-gray-600 dark:text-gray-dark-600">I'm a Final year IT student with hands-on
                  experience in HTML, CSS, JavaScript, Vue.js, and
                  modern web development practices. Seeking an opportunity to join a dynamic team where I can apply my
                  technical skills to build responsive, user-friendly, and high-performance web applications. Eager to
                  continuously improve my expertise, learn from experienced developers, and contribute to impactful
                  products that deliver excellent user experiences and business value.</p>
            </div>

            <div class="flex flex-col gap-2">
               <div class="flex gap-2 items-center text-gray-600 dark:text-gray-dark-600">
                  <IconsAddress />
                  <p class="leading-6">O Cho Dua, Ha Noi</p>
               </div>
               <div class="flex gap-2 items-center text-gray-600 dark:text-gray-dark-600">
                  <IconsDot />
                  <p class="leading-6">Available for new projects</p>
               </div>
            </div>

            <div class="flex gap-1 items-center">
               <a href="https://github.com/MinhQuan1912" target="_blank" rel="noopener noreferrer">
                  <IconsGithub class="text-gray-600 dark:text-gray-dark-600" />
               </a>
            </div>
         </div>
         <div class="flex w-100 items-center shrink-0 relative">
            <div class="absolute w-70 h-80 bg-white dark:bg-transparent bottom-0 right-0 p-2 z-1">
               <div class="w-full h-full bg-gray-200 dark:bg-gray-dark-200"></div>
            </div>
            <div class="absolute w-70 h-80 bg-white dark:bg-[#0f172b] bottom-10 right-10 p-2 z-2">
               <NuxtImg src="/images/quan.png" alt="Quan" class="w-full h-full object-cover" />
            </div>
         </div>
      </div>
   </div>
</template>

<script setup lang="ts">

</script>

<style scoped></style>