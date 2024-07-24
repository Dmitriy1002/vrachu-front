<script setup>
import { computed, defineComponent, onMounted, ref, watch } from 'vue'
import { Pagination, Navigation } from 'swiper/modules'
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/pagination'

const size = ref(111)
const perView = ref(3)
const width = ref(window.innerWidth)
const modules = [Pagination, Navigation]
const swiperFreshPickRef = ref(null)
const emit = defineEmits(['showPopup'])

onMounted(() => {
  calcWidth()
})

const calcWidth = () => {
  if (window.innerWidth < 790) {
    size.value = 31
    perView.value = 1
  } else {
    size.value = 111
    perView.value = 3
  }
}

window.addEventListener('resize', (event) => {
  calcWidth()
})

watch(
  () => width.value,
  () => {
    calcWidth()
  }
)

const prevSlide = () => {
  swiperFreshPickRef.value?.$el.swiper.slidePrev()
}

const nextSlide = () => {
  swiperFreshPickRef.value?.$el.swiper.slideNext()
}
</script>
<template>
  <div class="relative mt-[96px]">
    <div class="flex justify-between items-center xl:flex-row flex-col">
      <div class="text-center xl:text-start xl:pb-0 pb-6">
        <div class="text-[31px] leading-9 font-medium">Сертификаты врачей</div>
        <div class="text-[#7F7F7F] leading-6 text-[15px] font-light mt-6">
          Каждый врач проходит проверку наличия медицинского <br />
          образования и действующих сертификатов <br />
          специалистов.Также врачи проходят проверку <br />
          идентификации личности
        </div>
      </div>
      <div class="flex gap-6 items-center xl:w-auto w-full xl:h-auto h-full relative">
        <div class="flex w-full justify-between absolute z-50 top-1/2 translate-y-1/2">
          <div
            @click="prevSlide"
            :class="['arrow__prev lg:-translate-x-13 -translate-x-2 -translate-y-7']"
          >
            <div class="w-[48px] h-[48px] rounded-full bg-[#F2F2F2] p-3">
              <svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M15 18L9 12L15 6"
                  stroke="black"
                  stroke-width="1.5"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </div>
          </div>
          <div
            @click.stop="nextSlide"
            :class="['arrow__next xl:translate-x-13 translate-x-2 -translate-y-7']"
          >
            <div class="w-[48px] h-[48px] rounded-full bg-[#F2F2F2] p-3">
              <svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
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
        <Swiper
          class="swiper xl:h-[432px] h-[200px] xl:w-[820px] w-[calc(100%-90px)] block"
          :space-between="24"
          :modules="modules"
          :loop="true"
          ref="swiperFreshPickRef"
          :slides-per-view="perView"
          :navigation="true"
          :pagination="{ clickable: true }"
        >
          <SwiperSlide
            class="w-[25%] aspect-[0.7] bg-[#F2F2F2]"
            v-for="item in 5"
            :key="item"
          ></SwiperSlide>
        </Swiper>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
