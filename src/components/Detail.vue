<script setup>
import {defineProps} from 'vue'

defineProps(['avatarImg','title','descrition','duration','points','toolIcons'])

function getImgUrl(img) {
    return new URL(`../assets/images/${img}`, import.meta.url);
}
</script>
<template>
  <div class="flex flex-col md:flex-row items-center justify-between mt-4">
    <div class="flex gap-5">
      <img :src="getImgUrl(avatarImg)" alt="" class="w-10 h-10 rounded-full self-start object-contain" />
      <div>
        <h3 class="text-xl font-medium">{{ title }}</h3>
        <p class="text-lg font-medium">{{ descrition }} <span v-if="descrition" class="text-[40px]">.</span> <span class="text-gray-600">{{ duration }}</span></p>
        <ul class="list-inside list-disc">
          <li v-for="item in points" :key="item">{{ item }}</li>
        </ul>
      </div>
    </div>
    <div class=" flex flex-wrap gap-3 items-center justify-center w-full md:w-auto md:grid md:grid-cols-3 md:gap-4 self-start my-2 md:mt-6">
      <img v-for="imgSrc in toolIcons" :key="imgSrc" :src="getImgUrl(imgSrc)" alt="" class="w-9 h-9 object-contain" />
    </div>
  </div>
</template>
