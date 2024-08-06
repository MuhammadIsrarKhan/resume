<script setup>
import Hero from './views/Hero.vue'
import Toaster from '@/components/ui/toast/Toaster.vue'
import Detail from './components/Detail.vue'
</script>

<template>
  <div class="flex items-center gap-4 flex-col py-14 mx-4 lg:mx-32 xl:mx-64 2xl:mx-80">
    <Hero />
    <div class="flex flex-col gap-5 justify-between w-full print:mt-52">
      <h2 class="text-xl font-semibold">Work Experience</h2>
      <Detail
        avatarImg="antonx.jpeg"
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
          'html-5.png',
          'css-3.png',
          'tailwindcss.svg',
          'vuejs.svg',
          'pinia.png',
          'reactjs.png',
          'react-router.svg',
          'redux.svg',
          'react-query.jpeg'
        ]"
      />
      <Detail
        avatarImg="marq.png"
        title="marQnetworks"
        descrition="web developer"
        duration="Aug 2021 - Dec 2022"
        :points="[
          'I worked on their website of real state.',
          'design and integrate website with pure html css and javascript.'
        ]"
        :toolIcons="['html-5.png', 'css-3.png', 'js.png']"
      />
      <Detail
        avatarImg="techtrack.jpeg"
        title="Tech Track"
        descrition="Web Development Intern"
        duration="May 2021 - Sep 2021"
        :points="[
          'I learned HTML5,CSS3 and bootstrap in this internship.',
          'I designed invoices for different vendors which are customer of my company.',
          'designed pages for ERP in bootstrape.'
        ]"
        :toolIcons="['html-5.png', 'css-3.png', 'bootstrap.png']"
      />
    </div>
    <div class="flex flex-col justify-between w-full">
      <h2 class="text-xl font-semibold ">Education</h2>
      <Detail
        avatarImg="uet.jpeg"
        title="University of Engineering & Technology, Peshawar"
        duration="Sep 2018 - July 2022"
        :points="['Engineering Degree in computer systems.']"
      />
    </div>
    <div class="flex flex-col justify-between w-full">
      <h2 class="text-xl font-semibold">Side Projects</h2>
      <Detail
        avatarImg="watch-turks.svg"
        title="Watch Turks"
        duration="Nov 2022 - Jan 2023"
        :points="['The premium website for Turkish Series!.','I integrate apis in this website!.']"
        :toolIcons="[
          'tailwindcss.svg',
          'reactjs.png',
          'react-router.svg',
          'redux.svg',
          'react-query.jpeg'
        ]"
      />
      <Detail
        avatarImg="billbb.ico"
        title="Billbb Dashboard"
        duration="June 2024 - July 2024"
        :points="['Dashboard for managing data of mobile application!']"
        :toolIcons="[
          'nextjs-icon.svg',
          'nodejs.png',
          'reactjs.png',
          'redux.svg',
          'react-query.jpeg'
        ]"
      />
    </div>
    <div class="print:items-center print:justify-center hidden print:flex">
      <p class="flex gap-1 mb-2"> <img src="@/components/icons/world.svg" alt="" width="20px" height="20px" />Go to <a href="https://resume-nine-orcin.vercel.app/"><strong>https://misrarkhan.vercel.app/</strong></a> to see this resume in more details.</p>
    </div>
  </div>
  <Toaster />
</template>
