<script setup>
import { RouterLink, RouterView } from 'vue-router'

import IconLogo from '@/components/icons/IconLogo.vue'
import { ref } from 'vue'

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

const isOpen = ref(false)
const toggle = () => {
  if (!isOpen.value) {
    isOpen.value = !isOpen.value
    document.body.classList.add('_lock')
  } else {
    isOpen.value = !isOpen.value
    document.body.classList.remove('_lock')
  }
}
</script>
<template>
  <div class="">
    <div class="h-12">
      <img
        v-if="!isOpen"
        @click="toggle"
        class="ml-auto mt-7 cursor-pointer w-12"
        src="/hamburger-menu.svg"
        alt=""
      />
      <img v-else @click="toggle" class="w-12 ml-auto mt-7 cursor-pointer" src="/x.png" alt="" />
    </div>

    <Transition name="fade" duration="300">
      <div
        v-if="isOpen"
        class="fixed top-45 right-[2.5vw] w-[95vw] h-fit max-h-[calc(100vh-260px)] overflow-auto rounded-xl bg-[#d3e8f1] z-50 transition-all duration-300"
      >
        <div class="mt-[47px] flex flex-col justify-around overflow-auto">
          <div
            v-for="link in links"
            :key="link"
            class="text-[20px] group relative pt-5 cursor-pointer font-medium mx-4"
          >
            <div
              v-if="link.active"
              class="h-[3px] w-full bg-[#9CCF26] absolute bottom-0 rounded-full"
            ></div>
            <div
              class="group-hover:block hidden h-[3px] w-full bg-[#9CCF26] absolute bottom-0 rounded-full"
            ></div>
            <div @click="link.active = !link.active" class="w-full flex justify-between">
              <div>
                <p class="">
                  {{ link.name }}
                </p>
                <div v-for="item in link.children" :key="item" class="">
                  <Transition name="child">
                    <div v-if="link.active" class="">
                      <p class="pl-6 text-[#0008]">
                        {{ item.name }}
                      </p>
                    </div>
                  </Transition>
                </div>
              </div>
              <svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                class="rotate-90"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M9 18L15 12L9 6"
                  stroke="black"
                  stroke-width="1.5"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </div>
          </div>
        </div>
      </div>
    </Transition>
  </div>
</template>

<style sscoped>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.3s ease-in-out;
}

.fade-enter-from,
.fade-leave-to {
  transform: translateX(700px);
}
.child-enter-active,
.child-leave-active {
  transition: all 0.2s ease-in-out;
  height: 30px;
  opacity: 1;
}

.child-enter-from,
.child-leave-to {
  transform: translateX(10px);
  opacity: 0;
  height: 0;
}
</style>
