<template>
   <div id="Contact" class="container mx-auto">
      <div class=" py-24 flex flex-col gap-12 justify-between items-center">

         <div class="flex flex-col gap-4 justify-between items-center">
            <Tag text="Get in touch" />
            <p class="w-xl text-center text-xl leading-7 text-gray-600 dark:text-gray-dark-600">What's next? Feel free
               to reach out to me if you're looking for a developer, have a query, or
               simply want to connect.</p>
         </div>

         <div class="flex flex-col justify-between items-center gap-4">
            <div class="flex justify-between items-center gap-5 h-11">
               <IconsMail class="text-gray-600 dark:text-gray-dark-600" />
               <p class="font-semibold text-4xl leading-10 tracking-[-0.02em] text-gray-900 dark:text-gray-dark-900">{{
                  email }}</p>
               <CopyButton :text="email" />
            </div>
            <div class="flex justify-between items-center gap-5 h-11">
               <IconsPhone class="text-   gray-600 dark:text-gray-dark-600" />
               <p class="font-semibold text-4xl leading-10 tracking-[-0.02em] text-gray-900 dark:text-gray-dark-900">
                  {{ phone }}</p>
               <CopyButton :text="phone" />
            </div>
         </div>

         <div class="flex flex-col justify-between items-center gap-2">
            <p class="leading-6 text-gray-600 dark:text-gray-dark-600">You may also find me on these platforms!</p>
            <div class="flex gap-1 justify-center">
               <a href="https://github.com/MinhQuan1912" target="_blank" rel="noopener noreferrer">
                  <IconsGithub class="text-gray-600 dark:text-gray-dark-600" />
               </a>
            </div>
         </div>
      </div>
   </div>
   <div class="flex items-center justify-center py-6 gap-2 bg-gray-50 dark:bg-gray-dark-50 text-gray-600">
      <IconsCopyright class="text-gray-600 dark:text-gray-dark-600" />
      <p class="text-sm leading-5 text-gray-600 dark:text-gray-dark-600">2026 | Made by Minh Quan</p>
   </div>
</template>

<script setup lang="ts">
const email = 'nminhquan1912@gmail.com'
const phone = '0988 934 362'

</script>

<style scoped></style>