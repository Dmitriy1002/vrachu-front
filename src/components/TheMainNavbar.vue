<script setup>
import { RouterLink, RouterView } from 'vue-router'

import IconLogo from '@/components/icons/IconLogo.vue'
import { ref } from 'vue'

const isActiveOpener = ref(false)
const navBar = ref()
const OpenNavBar = () => {
  console.log('oisso')
  isActiveOpener.value = true
}
const CloseNavBar = () => {
  console.log('oio')
  isActiveOpener.value = false
}

const links = ref([
  {
    name: 'Главная',
    active: true,
    children: [
      { name: 'blablabla', active: true },
      { name: 'blablabla' },
      { name: 'blablabla' },
      { name: 'blablabla' },
      { name: 'blablabla' }
    ]
  },
  {
    name: 'Консультации',
    children: [
      { name: 'blablabla' },
      { name: 'blablabla' },
      { name: 'blabladssddsbla' },
      { name: 'blablabla' },
      { name: 'blablabla' }
    ]
  },
  {
    name: 'Врачи',
    children: [
      { name: 'blablabsdsdla' },
      { name: 'blablabla' },
      { name: 'blablabla' },
      { name: 'blablabla' }
    ]
  },
  {
    name: 'Статьи',
    children: [{ name: 'blablabla' }, { name: 'blablabla' }, { name: 'blablabla' }]
  },
  {
    name: 'Помощь',
    children: [
      { name: 'blablabla' },
      { name: 'blablabla' },
      { name: 'blablabla' },
      { name: 'blablabla' },
      { name: 'blablabla' }
    ]
  },
  {
    name: 'Врачам',
    children: [
      { name: 'blablabla' },
      { name: 'blablabla' },
      { name: 'blabldssabla' },
      { name: 'blablabla' },
      { name: 'blablabla' }
    ]
  },
  {
    name: 'Контакты',
    children: [{ name: 'blablabla' }, { name: 'blablabla' }]
  }
])
</script>
<template>
  <div class="relative">
    <Transition name="fade2">
      <div
        v-if="isActiveOpener"
        class="bg-[#9CCF26] p-1 w-[calc(100%)] z-[10] h-20 justify-around absolute top-20 right-0"
      ></div>
    </Transition>
    <div class="absolute z-[80] top-0 right-0 w-[calc(100%-0px)]">
      <div
        ref="navBar"
        @mouseenter="OpenNavBar"
        @mouseleave="CloseNavBar"
        class="mt-[47px] border-[#9CCF2680] border-4 bg-[#CEE793] flex flex-col rounded-[33px] justify-around overflow-auto"
      >
        <div class="flex relative rounded-[33px] justify-around bg-white">
          <div
            v-for="link in links"
            :key="link"
            class="text-[15px] relative py-5 cursor-pointer font-medium mx-4"
          >
            <div
              v-if="link.active"
              class="h-[6px] w-full bg-[#9CCF26] absolute bottom-0 rounded-t-full"
            ></div>

            {{ link.name }}
          </div>
        </div>
      </div>

      <Transition name="fade2">
        <div
          v-if="isActiveOpener"
          class="bg-[#9CCF26] p-1 w-[calc(100%)] h-fit z-[70] flex rounded-[33px] justify-around absolute top-30"
        >
          <!-- <div class="bg-[#9CCF26] p-1 w-[calc(100%)] h-20 justify-around absolute -top-10"></div> -->
          <div class="bg-[#fff] w-full flex rounded-[33px] justify-around top-50">
            <div
              v-for="link in links"
              :key="link"
              class="text-[15px] mt-3 relative cursor-pointer font-medium"
            >
              <div
                v-for="item in link.children"
                :key="item"
                class="py-[13px] text-center xl:px-4 px-2 rounded-full mb-1 hover:bg-[#f4f3f371]"
                :class="item.active ? 'bg-[#F4F3F3]' : 'bg-white'"
              >
                {{ item.name }}
              </div>
            </div>
          </div>
        </div>
      </Transition>
    </div>
  </div>
</template>

<style scoped>
.fade2-enter-active,
.fade2-leave-active {
  transition: all 0.3s ease-in-out;
  opacity: 1;
}

.fade2-enter-from,
.fade2-leave-to {
  opacity: 0;
}
</style>
