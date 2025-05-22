<script setup>
import { defineProps } from 'vue'
import TooltipComponent from '@/components/Tooltip.vue'

defineProps(['avatarImg', 'title', 'descrition', 'duration', 'points', 'toolIcons'])

function getImgUrl(img) {
  return new URL(`../assets/images/${img}`, import.meta.url)
}

// Extract filename without extension for displaying in tooltips
function getDisplayName(filename) {
  return filename.split('.')[0].replace(/-/g, ' ')
}
</script>
<template>
  <div class="flex flex-col md:flex-row items-center justify-between mt-4">
    <div class="flex gap-5">
      <img
        :src="getImgUrl(avatarImg)"
        alt=""
        class="w-10 h-10 rounded-full self-start object-contain"
      />
      <div>
        <h3 class="text-xl font-medium">{{ title }}</h3>
        <p class="text-lg font-medium">
          {{ descrition }} <span v-if="descrition" class="text-[40px]">.</span>
          <span class="text-gray-600">{{ duration }}</span>
        </p>
        <ul class="list-inside list-disc max-w-[650px]">
          <li v-for="item in points" :key="typeof item === 'object' ? item.text : item">
            <template v-if="typeof item === 'object' && item.url">
              <template v-if="item.text.includes(':')">
                <span>{{ item.text.split(':')[0] }}: </span>
                <a :href="item.url" target="_blank" class="text-blue-600 hover:underline">{{
                  item.text.split(':')[1].trim()
                }}</a>
              </template>
              <template v-else>
                <a :href="item.url" target="_blank" class="text-blue-600 hover:underline">{{
                  item.text
                }}</a>
              </template>
            </template>
            <template v-else>{{ item }}</template>
          </li>
        </ul>
      </div>
    </div>    <div
      class="flex flex-wrap gap-3 items-center justify-center w-full md:w-auto md:grid md:grid-cols-3 md:gap-4 self-start my-2 md:mt-6"
    >
      <TooltipComponent v-for="imgSrc in toolIcons" :key="imgSrc">
        <img
          :src="getImgUrl(imgSrc)"
          alt=""
          class="w-10 h-10 object-contain"
        />
        <template #tooltipContent>
          {{ getDisplayName(imgSrc) }}
        </template>
      </TooltipComponent>
    </div>
  </div>
</template>
