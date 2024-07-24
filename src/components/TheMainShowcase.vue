<script setup>
import IconLogo from '@/components/icons/IconLogo.vue'
import IconSearch from '@/components/icons/IconSearch.vue'
import IconMainFav from '@/components/icons/IconMainFav.vue'
import TheMainNavbar from '@/components/TheMainNavbar.vue'
import { onMounted, ref } from 'vue'
import { useIntersectionObserver } from '@vueuse/core'

const target = ref(null)
const targetIsVisible = ref(false)

const updateCount = () => {
  const counters = document.querySelectorAll('.counters')
  const speed = 15
  counters.forEach((counter) => {
    const update = () => {
      let target = +counter.getAttribute('data-target')
      let count = +counter.innerText.replaceAll(' ', '')
      let inc = target / speed
      if (count < target) {
        counter.innerText = new Intl.NumberFormat('en-US')
          .format(Math.ceil(count + inc))
          .replace(/,/g, ' ')
        setTimeout(update, 25)
      } else {
        counter.innerText = target
        const formattedNumber = new Intl.NumberFormat('en-US').format(target).replace(/,/g, ' ')
        console.log(formattedNumber)
        counter.innerText = formattedNumber
      }
    }
    counter.innerText = 0
    update()
  })
}

const { stop } = useIntersectionObserver(target, ([{ isIntersecting }], observerElement) => {
  targetIsVisible.value = isIntersecting
  if (isIntersecting) {
    updateCount()
  }
})
</script>
<template>
  <div
    ref="target"
    class="relative xl:mt-[73px] text-center mt-[30px] flex justify-center xl:flex-row flex-col"
  >
    <div class="xl:mt-0 mt-4 pr-[36px] pl-[42px] border-r-[1px] border-[#E6E6E6]">
      <div
        :data-target="2229377"
        class="counters mx-auto text-[55px] w-[280px] text-[#9CCF26] font-medium leading-[36px] xl:text-start text-center"
      >
        0
      </div>
      <div class="text-[17px] leading-[24px] font-light mt-[12px] ml-1 xl:text-start text-center">
        вопросов
      </div>
    </div>
    <div class="xl:mt-0 mt-4 pr-[36px] pl-[42px] border-r-[1px] border-[#E6E6E6]">
      <div
        :data-target="14518050"
        class="counters mx-auto text-[55px] w-[300px] text-[#9CCF26] font-medium leading-[36px] xl:text-start text-center"
      >
        0
      </div>
      <div class="text-[17px] leading-[24px] font-light mt-[12px] ml-3.5 xl:text-start text-center">
        врачей на сайте
      </div>
    </div>
    <div class="xl:mt-0 mt-4 pr-[36px] pl-[42px]">
      <div
        :data-target="17116"
        class="counters mx-auto text-[55px] w-[180px] text-[#9CCF26] font-medium leading-[36px] xl:text-start text-center"
      >
        0
      </div>
      <div class="text-[17px] leading-[24px] font-light mt-[12px] ml-3.5 xl:text-start text-center">
        врачей на сайте
      </div>
    </div>
  </div>
</template>

<style scoped>
.intersection-div {
  width: 100px;
  height: 100px;
  /* background-color: lightblue; */
  margin: 20px;
}
.intersection-div.intersection {
  background-color: lightgreen;
}
</style>
