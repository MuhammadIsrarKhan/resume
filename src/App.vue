<script setup>
import Hero from './views/Hero.vue';
import Toaster from '@/components/ui/toast/Toaster.vue'
import Detail from './components/Detail.vue';

</script>

<template>
  <div class="flex items-center gap-4 flex-col pt-14 mx-80">
   <Hero />
   <div class="flex flex-col justify-between w-full">
     <h2 class="text-xl font-semibold">Work Experience</h2>
     <Detail title="Tech Track" descrition="Web Development Intern" :points="['Work in progress']" :toolIcons="['/src/assets/images/vuejs.svg','/src/assets/images/vuejs.svg','/src/assets/images/vuejs.svg']" />
   </div>
  </div>
  <Toaster />
</template>
