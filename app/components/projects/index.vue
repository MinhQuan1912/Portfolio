<template>
   <div id="Projects" class="container mx-auto">
      <div class="flex flex-col py-24 px-8 gap-12">
         <div class="flex flex-col items-center gap-4">
            <Tag text="Projects" />
            <p class="text-center text-xl leading-7 text-gray-600 dark:text-gray-dark-600">Some of the noteworthy
               projects I have built</p>
         </div>
         <div class="flex flex-col items-center gap-12 px-8">
            <div v-for="project in list" class="flex w-full h-120 shadow-md rounded-xl">
               <div class="w-1/2 p-12 bg-gray-50 dark:bg-gray-dark-200 drop-shadow-md">
                  <Swiper :modules="[Navigation, Pagination, Autoplay]" :slides-per-view="1" :loop="true"
                     :pagination="{ clickable: true }"
                     :navigation="true" :autoplay="{ delay: 3000, disableOnInteraction: false }"
                     class="rounded-xl drop-shadow-lg overflow-hidden w-120 h-96">
                     <SwiperSlide v-for="image in project.images" :key="image">
                        <NuxtImg :src="image" class="h-full w-full object-fill " />
                     </SwiperSlide>
                  </Swiper>
               </div>
               <div class="w-1/2 p-12 flex flex-col gap-6 dark:bg-gray-dark-100">
                  <p class="font-semibold text-xl leading-7 text-gray-900 dark:text-gray-dark-900">{{ project.name }}
                  </p>
                  <p class="leading-6 text-gray-600 dark:text-gray-dark-600">{{ project.description }}</p>
                  <div class="flex flex-wrap gap-2">
                     <Tag v-for="tech in project.technologies" :text="tech" />
                  </div>
                  <div class="flex gap-4">
                     <NuxtLink :to="project.link.github" target="_blank" rel="noopener noreferrer"
                        class="flex gap-2 items-center py-1.5 px-4 rounded-xl border-0 bg-gray-900 dark:bg-gray-dark-900 text-gray-50 dark:text-gray-dark-50 font-medium leading-6 
                        hover:text-gray-dark-50 hover:bg-gray-dark-900 dark:hover:text-gray-50 dark:hover:bg-gray-900 transition duration-200 ease-in-out">
                        <IconsGithub />
                        View
                        on GitHub
                     </NuxtLink>
                     <NuxtLink :to="project.link.live" target="_blank" rel="noopener noreferrer"
                        class="flex gap-2 items-center py-1.5 px-4 rounded-xl border-0 bg-gray-900 dark:bg-gray-dark-900 text-gray-50 dark:text-gray-dark-50 font-medium leading-6 
                        hover:text-gray-dark-50 hover:bg-gray-dark-900 dark:hover:text-gray-50 dark:hover:bg-gray-900 transition duration-200 ease-in-out">
                        <IconsLink />
                        Live Demo
                     </NuxtLink>
                  </div>

               </div>

            </div>
         </div>
      </div>
   </div>
</template>

<script setup lang="ts">
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import { Navigation, Pagination, Autoplay } from 'swiper/modules'
const list = [
   {
      images: ['/images/project1/image1.png', '/images/project1/image2.png', '/images/project1/image3.png', '/images/project1/image4.png'],
      name: 'TechZone',
      description: 'An e-commerce website for tech products consisting of three separate applications: a customer storefront, an admin dashboard, and an API server. It includes key features such as secure authentication, online payments, automated order management, and real-time chat. The project was developed independently to simulate the end-to-end process of building and deploying a production-ready software product.',
      technologies: ['Nuxt', 'NestJs', 'MySQL', 'Tailwind CSS', 'TypeScript', 'Git'],
      link: {
         github: 'https://github.com/MinhQuan1912/TechZoneWebsite',
         live: 'https://techzone-a38268.netlify.app'
      }
   }
]
</script>

<style scoped></style>