<script setup>
import { useToast } from '@/components/ui/toast/use-toast'
import { Avatar, AvatarFallback, AvatarImage } from '@/components/ui/avatar'
import { Badge } from '@/components/ui/badge'
import { MessagesSquare } from 'lucide-vue-next'
import Button from '@/components/ui/button/Button.vue'
import Tooltip from '@/components/Tooltip.vue'
import { ref } from 'vue'
import { useClipboard } from '@vueuse/core'
import {
  Heart,
  Laptop,
  GraduationCap,
  TowerControl,
  ScanText,
  Target,
  ShieldHalf,
  MapPin
} from 'lucide-vue-next'

const source = ref('israruetp@gmail.com')
const { toast } = useToast()
const { copy } = useClipboard({ source })
function getImgUrl() {
  return new URL(`../assets/profile.jpg`, import.meta.url)
}
</script>
<template>
  <div class="flex md:gap-32 justify-between print:md:gap-4 w-full">
    <div>
      <h1 class="text-3xl font-semibold">Muhammad Israr Khan</h1>
      <p class="text-lg font-normal my-1">
        Versatile Software Engineer, crafting challenging products <br />
        with extra attention to detail. 3+ years of experience.
      </p>
      <div class="flex gap-1 mb-2">
        <!-- <img src="@/components/icons/world.svg" alt="" width="20px" height="20px" /> -->
        <MapPin class="w-5 h-5" />
        <p class="text-sm">Peshawar, Pakistan</p>
      </div>
      <div class="flex gap-3 mt-2.5 print:hidden">
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
    <div class="hidden print:block">
      <ul class="flex flex-col gap-4">
        <li class="flex gap-2 items-start">
          <img src="@/components/icons/mail.svg" alt="" class="w-4 h-4" />
          <p class="-translate-y-1">israruetp@gmail.com</p>
        </li>
        <li class="flex gap-2 items-start">
          <img src="@/components/icons/github.svg" alt="" class="w-4 h-4" />
          <p class="-translate-y-1">https://github.com/MuhammadIsrarKhan</p>
        </li>
        <li class="flex gap-2 items-start">
          <img src="@/components/icons/linkedin.svg" alt="" class="w-4 h-4" />
          <p class="-translate-y-1">https://www.linkedin.com/in/muhammad-israr-khan-558300199/</p>
        </li>
      </ul>
    </div>
    <div>
      <Avatar class="w-16 h-16 md:w-32 md:h-32">
        <AvatarImage :src="getImgUrl()" alt="@radix-vue" />
        <AvatarFallback>MIK</AvatarFallback>
      </Avatar>
    </div>
  </div>
  <div class="flex flex-col md:flex-row gap-y-6 md:justify-between w-full print:mt-1">
    <div class="flex gap-2 flex-col print:gap-4">
      <h2 class="text-xl font-semibold">Main Tools</h2>
      <div class="flex gap-2">
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/html-5.png" alt="" class="w-4 h-4" /> HTML5</Badge
        >
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/css-3.png" alt="" class="w-4 h-4" />CSS3</Badge
        >
      </div>
      <Badge
        class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
        ><img src="@/assets/images/tailwindcss.svg" alt="" class="w-4 h-4" />css utility
        frameworks</Badge
      >
      <div class="flex gap-2">
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/js.png" alt="" class="w-4 h-4" /> Javascript</Badge
        >
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/typescript.svg" alt="" class="w-4 h-4" />Typescript</Badge
        >
      </div>
      <div class="flex gap-2">
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/reactjs.png" alt="" class="w-4 h-4" /> React js</Badge
        >
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/nextjs-icon.svg" alt="" class="w-4 h-4" /> Next js</Badge
        >
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/vuejs.svg" alt="" class="w-4 h-4" /> vue js</Badge
        >
      </div>
      <div class="flex gap-2">
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/nodejs.png" alt="" class="w-4 h-4" />Node js</Badge
        >
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/php.png" alt="" class="w-4 h-4" />PHP</Badge
        >
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/firebase.png" alt="" class="w-4 h-4" /> Firebase</Badge
        >
        <Badge
          class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          ><img src="@/assets/images/docker.png" alt="" class="w-4 h-4" /> Docker</Badge
        >
      </div>
    </div>
    <div class="flex gap-2 flex-col print:gap-4">
      <h2 class="text-xl font-semibold">Roles</h2>
      <Tooltip>
        <template #default>
          <Badge
            class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          >
            <Laptop class="w-4 h-4 print:text-black" /> Frontend Developer</Badge
          >
        </template>
        <template #tooltipContent>
          <p>
            I build entire web frontend with react <br />
            js OR vue js.
          </p>
        </template>
      </Tooltip>
      <Tooltip>
        <template #default>
          <Badge
            class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          >
            <GraduationCap class="w-4 h-4 print:text-black" /> Frondend Lead</Badge
          >
        </template>
        <template #tooltipContent>
          <p>
            I help junior developers to level up, by <br />
            showing besct practices.
          </p>
        </template>
      </Tooltip>
      <Tooltip>
        <template #default>
          <Badge
            class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          >
            <TowerControl class="w-4 h-4 print:text-black" />
            360° Vision
          </Badge>
        </template>
        <template #tooltipContent>
          <p>
            I blend tech expertise with key startup <br />
            facets: product, UX, business strategy, <br />
            and market, to drive effective solutions.
          </p>
        </template>
      </Tooltip>
    </div>
    <div class="flex gap-2 flex-col print:gap-4">
      <h2 class="text-xl font-semibold">Values</h2>
      <Tooltip>
        <template #default>
          <Badge
            class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
            ><ScanText class="w-4 h-4 print:text-black" /> Autonomy & Ownership</Badge
          >
        </template>
        <template #tooltipContent>
          <p>
            I can take complex tasks and get things <br />
            done with strong focus.
          </p>
        </template>
      </Tooltip>
      <Tooltip>
        <template #default>
          <Badge
            class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
          >
            <Target class="w-4 h-4 print:text-black" /> High level of requirement</Badge
          >
        </template>
        <template #tooltipContent>
          <p>
            I pay high attention to details and try to <br />
            deliver the best solution, because <br />
            making things work is not enough.
          </p>
        </template>
      </Tooltip>
      <Tooltip>
        <template #default>
          <Badge
            class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
            ><Heart class="w-4 h-4 print:text-black" /> Healthy relationship</Badge
          >
        </template>
        <template #tooltipContent>
          <p>
            I truly value workspaces full of trust, honesty <br />
            and kindness.
          </p>
        </template>
      </Tooltip>
      <Tooltip>
        <template #default>
          <Badge
            class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
            ><ShieldHalf class="w-4 h-4 print:text-black" /> Team Spirit</Badge
          >
        </template>
        <template #tooltipContent>
          <p>
            I believe collaborative efforts and a <br />
            supportive environment are essential <br />
            for achieving collective success.
          </p>
        </template>
      </Tooltip>
      <Tooltip>
        <template #default>
          <Badge
            class="flex items-center justify-center text-sm gap-2 font-medium bg-gray-700 hover:bg-black w-fit print:border-gray-400 print:text-black"
            ><MessagesSquare class="w-4 h-4" /> Active Cummunication</Badge
          >
        </template>
        <template #tooltipContent>
          <p>
            I Listen, explain, document, draw, and use <br />
            both async & sync communication.
          </p>
        </template>
      </Tooltip>
    </div>
  </div>
</template>
