<script setup>
import { useToast } from '@/components/ui/toast/use-toast'
import { Avatar, AvatarFallback, AvatarImage } from '@/components/ui/avatar'
import { Badge } from '@/components/ui/badge'
import { MessagesSquare } from 'lucide-vue-next';
import Button from '@/components/ui/button/Button.vue'
import Tooltip from '@/components/Tooltip.vue'
import { ref } from 'vue'
import { useClipboard } from '@vueuse/core'

const source = ref('israruetp@gmail.com')
const { toast } = useToast()
const { text, copy, copied } = useClipboard({ source })
</script>
<template>
     <div class="flex gap-32 justify-between w-full">
      <div>
        <h1 class="text-3xl font-semibold">Muhammad Israr Khan</h1>
        <p class="text-lg font-normal my-1">
          Versatile Software Engineer, crafting challenging products <br />
          with extra attention to detail. 2+ years of experience.
        </p>
        <div class="flex gap-1 mb-2">
          <img src="@/components/icons/world.svg" alt="" width="20px" height="20px" />
          <p class="text-sm">Peshawar, Pakistan</p>
        </div>
        <div class="flex gap-3 mt-2.5">
          <div
            @click="
              () => {
                copy(source)
                toast({
                  title: 'Cpoied!',
                  description: `${source} has been copied to your clipboard.`
                })
              }
            "
          >
            <Tooltip>
              <template #default>
                <Button variant="outline" size="icon"
                  ><img src="@/components/icons/mail.svg" alt="" class="w-4 h-4" />
                </Button>
              </template>
              <template #tooltipContent>
                <p>Copy my email address</p>
              </template>
            </Tooltip>
          </div>
          <Tooltip>
            <template #default>
              <a href="https://github.com/MuhammadIsrarKhan" target="_blank">
                <Button variant="outline" size="icon"
                  ><img src="@/components/icons/github.svg" alt="" class="w-4 h-4" />
                </Button>
              </a>
            </template>
            <template #tooltipContent>
              <p>Go to Github in page</p>
            </template>
          </Tooltip>
          <Tooltip>
            <template #default>
              <a href="https://www.linkedin.com/in/muhammad-israr-khan-558300199/" target="_blank">
                <Button variant="outline" size="icon"
                  ><img src="@/components/icons/linkedin.svg" alt="" class="w-4 h-4" />
                </Button>
              </a>
            </template>
            <template #tooltipContent>
              <p>Go to Linked in page</p>
            </template>
          </Tooltip>
        </div>
      </div>
      <div>
        <Avatar class="w-32 h-32">
          <AvatarImage src="/src/assets/profile.jpg" alt="@radix-vue" />
          <AvatarFallback>CN</AvatarFallback>
        </Avatar>
      </div>
    </div>
    <div class="flex justify-between w-full">
      <div class="flex gap-2 flex-col">
        <h2 class="text-xl font-semibold">Main Tools</h2>
        <div class="flex gap-2">
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/vuejs.svg" alt="" class="w-4 h-4" /> vue js</Badge
          >
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/reactjs.png" alt="" class="w-4 h-4" /> React js</Badge
          >
        </div>
        <div class="flex gap-2">
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/tailwindcss.svg" alt="" class="w-4 h-4" /> tailwind
            css</Badge
          >
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/typescript.svg" alt="" class="w-4 h-4" />Typescript</Badge
          >
        </div>
        <div class="flex gap-2">
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/js.png" alt="" class="w-4 h-4" /> Javascript</Badge
          >
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/php.png" alt="" class="w-4 h-4" />PHP</Badge
          >
        </div>
        <div class="flex gap-2">
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/html-5.png" alt="" class="w-4 h-4" /> HTML5</Badge
          >
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/css-3.png" alt="" class="w-4 h-4" />CSS3</Badge
          >
        </div>
      </div>
      <div class="flex gap-2 flex-col">
        <h2 class="text-xl font-semibold">Roles</h2>
        <Badge
          class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
          ><img src="@/assets/images/laptop.svg" alt="" class="w-4 h-4" /> Frontend Developer</Badge
        >
        <Badge
          class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
          ><img src="@/assets/images/hat.svg" alt="" class="w-4 h-4" /> Frondend Lead</Badge
        >
        <Badge
          class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
          ><img src="@/assets/images/lighthouse.svg" alt="" class="w-4 h-4" />
          360° Vision
        </Badge>
      </div>
      <div class="flex gap-2 flex-col">
        <h2 class="text-xl font-semibold">Values</h2>

          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/scan.svg" alt="" class="w-4 h-4" /> Autonomy & Ownership</Badge
          >
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/target.svg" alt="" class="w-4 h-4" /> High level of requirement</Badge
          >
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/heart.svg" alt="" class="w-4 h-4" /> Healthy relationship</Badge
          >
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><img src="@/assets/images/team.svg" alt="" class="w-4 h-4" />Team Spirit</Badge
          >
          <Badge
            class="flex items-center justify-center text-base gap-2 font-medium bg-gray-700 hover:bg-black w-fit"
            ><MessagesSquare class="w-4 h-4" /> Active Cummunication</Badge
          >
          
      </div>
    </div>
</template>