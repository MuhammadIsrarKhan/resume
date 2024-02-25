<script setup>
import {defineProps} from 'vue'
defineProps(['title','descrition','points','toolIcons'])
</script>
<template>
  <div class="flex items-center justify-between mt-4">
    <div class="flex gap-5">
      <img src="@/assets/images/js.png" alt="" class="w-10 h-10 rounded-full self-start" />
      <div>
        <h3 class="text-xl font-medium">{{ title }}</h3>
        <p class="text-lg font-normal">{{ descrition }}</p>
        <ul class="list-inside list-disc">
          <li v-for="item in points" :key="item">{{ item }}</li>
        </ul>
      </div>
    </div>
    <div class="grid grid-cols-3 gap-4">
      <img v-for="imgSrc in toolIcons" :key="imgSrc" :src="imgSrc" alt="" class="w-8 h-8" />
    </div>
  </div>
</template>
