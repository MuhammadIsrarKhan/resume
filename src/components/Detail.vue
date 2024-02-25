<script setup>
import {defineProps} from 'vue'

defineProps(['avatarImg','title','descrition','duration','points','toolIcons'])

function getImgUrl(img) {
    return new URL(`../assets/images/${img}`, import.meta.url);
}
</script>
<template>
  <div class="flex items-center justify-between mt-4">
    <div class="flex gap-5">
      <img :src="getImgUrl(avatarImg)" alt="" class="w-10 h-10 rounded-full self-start" />
      <div>
        <h3 class="text-xl font-medium">{{ title }}</h3>
        <p class="text-lg font-medium">{{ descrition }} <span class="text-[40px]">.</span> <span class="text-gray-600">{{ duration }}</span></p>
        <ul class="list-inside list-disc">
          <li v-for="item in points" :key="item">{{ item }}</li>
        </ul>
      </div>
    </div>
    <div class="grid grid-cols-3 gap-4 self-start mt-6">
      <img v-for="imgSrc in toolIcons" :key="imgSrc" :src="getImgUrl(imgSrc)" alt="" class="w-8 h-8" />
    </div>
  </div>
</template>
