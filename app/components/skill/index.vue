<template>
   <div class="container mx-auto">
      <div class="flex flex-col py-24 px-8 gap-12">
         <div class="flex flex-col items-center gap-4">
           <Tag text="Skills" />
            <p class="text-center text-xl leading-7 text-gray-600 dark:text-gray-dark-600">The skills, tools and
               technologies I good at</p>
         </div>
         <div class="flex flex-wrap items-center gap-x-20 gap-y-12">
            <div v-for="item in list" class="flex flex-col gap-2 items-center">
               <NuxtImg :src="item.image" alt="item.name" class="object-contain h-16 w-16"/>
               <p class="text-lg leading-7 text-gray-600 dark:text-gray-dark-600">{{ item.name }}</p>
            </div>
         </div>
      </div>
   </div>
</template>

<script setup lang="ts">
const list = [
   {
      image: '/images/javascript.png',
      name: 'JavaScript',
   },
   {
      image: '/images/typescript.png',
      name: 'TypeScript',
   },
   {
      image: '/images/vue.png',
      name: 'Vue Js',
   },
   {
      image: '/images/nuxt.png',
      name: 'Nuxt',
   },
   {
      image: '/images/nest.png',
      name: 'Nest Js',
   },
   {
      image: '/images/mysql.png',
      name: 'MySQL',
   },
   {
      image: '/images/tailwind.png',
      name: 'Tailwind CSS',
   },
   {
      image: '/images/git.png',
      name: 'Git',
   },
]
</script>

<style scoped>

</style>