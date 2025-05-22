<script setup>
import Hero from './views/Hero.vue'
import Toaster from '@/components/ui/toast/Toaster.vue'
import Detail from './components/Detail.vue'
</script>

<template>
  <div class="flex items-center gap-4 flex-col py-14 mx-4 lg:mx-32 xl:mx-52 2xl:mx-80">
    <Hero />
    <div class="flex flex-col gap-5 justify-between w-full print:mt-52">
      <h2 class="text-xl font-semibold">Work Experience</h2>
      <Detail
        avatarImg="antonx.jpeg"
        title="AntonX"
        descrition="E2 : Software Development Engineer - 1"
        duration="Sep 2022 - Present"
        :points="[
          'SDE-1 at Antonx, working on a SaaS Point of Sale (POS) system as a Full-Stack Web Developer.',
          'Developing and maintaining features using Vue Js, React.js,Next.js Node.js,Nest.js and Laravel.',
          'Assisting fellow developers and mentoring junior team members to resolve technical challenges.',
          'Contributing to performance optimization, scalability, and security of the SaaS POS system.',
          'Ensuring seamless integration of frontend and backend components for an efficient user experience.',
          {
            text: 'App #1: a website for finding EV stations in finland.',
            url: 'https://evseek.vercel.app/'
          },
          { text: 'App #2: a website for statup portals.', url: 'https://startupconnect.pk/' },
          {
            text: 'App #3: a website for buying, renting and selling property in saudia arabia.',
            url: 'https://ewanc.com/'
          },
          {
            text: 'App #4: HalalHMC is a React.js and Tailwind CSS–powered platform that lets UK Muslims confidently verify the genuine Halal status of their meat and food products.',
            url: 'https://weborders.gethalalnow.com/'
          },
          {
            text: 'App #5: A Web App that enables businesses to manage sales, inventory, and customer transactions efficiently in a cloud-based environment.',
            url: 'https://edge.unifiedbynow.com'
          }
        ]"
        :toolIcons="[
          'HTML5.png',
          'CSS3.png',
          'tailwindcss.svg',
          'Javascript.png',
          'Typescript.svg',
          'vuejs.svg',
          'pinia.png',
          'zustand.svg',
          'reactjs.png',
          'react-router.svg',
          'redux.svg',
          'react-query.jpeg',
          'Nextjs.svg',
          'laravel.webp',
          'Nestjs.png'
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
        :toolIcons="['HTML5.png', 'CSS3.png', 'Javascript.png']"
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
        :toolIcons="['HTML5.png', 'CSS3.png', 'Bootstrap.png']"
      />
    </div>
    <div class="flex flex-col justify-between w-full">
      <h2 class="text-xl font-semibold">Education</h2>
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
        avatarImg="Ashtra-workspace.svg"
        title="Ashtra Workspace Dashboard"
        duration="Nov 2024 - present"
        :points="[
          {
            text: 'Ashtra integrates advanced AI tools with essential business management features—seamless payments, intelligent scheduling, customer engagement, marketplace, marketing, and more—to help businesses thrive.',
            url: 'https://dashboard.ashtra.ai/'
          },
          'Working on a Ashtra workspace dashboard system as a Full-Stack Web Developer.',
          'Developing and maintaining features using Next.js ,Nest.js.'
        ]"
        :toolIcons="[
          'tailwindcss.svg',
          'Nextjs.svg',
          'zustand.svg',
          'react-query.jpeg',
          'Nestjs.png',
        ]"
      />
      <Detail
        avatarImg="watch-turks.svg"
        title="Watch Turks"
        duration="Nov 2022 - Jan 2023"
        :points="[
          { text: 'The premium website for Turkish Series!.', url: 'https://watchturks.online/' },
          'I integrate apis in this website!.'
        ]"
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
        :points="[
          {
            text: 'Dashboard for managing data of mobile application!',
            url: 'https://testfrontend.billbbtest.site'
          }
        ]"
        :toolIcons="['Nextjs.svg', 'nodejs.png', 'reactjs.png', 'redux.svg', 'react-query.jpeg']"
      />
    </div>
    <div class="print:items-center print:justify-center hidden print:flex">
      <p class="flex gap-1 mb-2">
        <img src="@/components/icons/world.svg" alt="" width="20px" height="20px" />Go to
        <a href="https://resume-nine-orcin.vercel.app/"
          ><strong>https://misrarkhan.vercel.app/</strong></a
        >
        to see this resume in more details.
      </p>
    </div>
  </div>
  <Toaster />
</template>
