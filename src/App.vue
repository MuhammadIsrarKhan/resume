<script setup>
import Hero from './views/Hero.vue'
import Toaster from '@/components/ui/toast/Toaster.vue'
import Detail from './components/Detail.vue'
</script>

<template>
  <div class="flex items-center gap-4 flex-col py-14 mx-4 lg:mx-32 xl:mx-64 2xl:mx-80">
    <Hero />
    <div class="flex flex-col justify-between w-full">
      <h2 class="text-xl font-semibold">Work Experience</h2>
      <Detail
        avatarImg="/src/assets/images/techtrack.jpeg"
        title="Tech Track"
        descrition="Web Development Intern"
        duration="May 2021 - Sep 2021"
        :points="[
          'I learned HTML5,CSS3 and bootstrap in this internship.',
          'I designed invoices for different vendors which are customer of my company.',
          'designed pages for ERP in bootstrape.'
        ]"
        :toolIcons="[
          '/src/assets/images/html-5.png',
          '/src/assets/images/css-3.png',
          '/src/assets/images/bootstrap.png'
        ]"
      />
      <Detail
        avatarImg="/src/assets/images/antonx.jpeg"
        title="AntonX"
        descrition="Associate Software Engineer"
        duration="Sep 2022 - Present"
        :points="[
          'In AntonX i learned and worked mainly on frontend teachnologies.',
          'I designed and developed 3 apps from the ground up and one is in progress.',
          'App #1: a website for finding EV stations in finland.',
          'App #2: a website for statup portals.',
          'App #3: a website for buying, renting and selling property in saudia arabia.',
          'Currently i am working on a website. which is food ordering app in uk.'
        ]"
        :toolIcons="[
          '/src/assets/images/html-5.png',
          '/src/assets/images/css-3.png',
          '/src/assets/images/tailwindcss.svg',
          '/src/assets/images/vuejs.svg',
          '/src/assets/images/pinia.png',
          '/src/assets/images/reactjs.png',
          '/src/assets/images/react-router.svg',
          '/src/assets/images/redux.svg',
        ]"
      />
    </div>
  </div>
  <Toaster />
</template>
