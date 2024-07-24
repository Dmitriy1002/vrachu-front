<template>
  <div class="mt-[136px]">
    <div class="text-[31px] leading-[36px] font-medium">Отзывы наших пользователей</div>
    <div class="md:mt-[58px] mt-[28px] relative">
      <div class="music-playlist__title">
        <div class="flex w-full justify-between absolute z-50 top-1/2 translate-y-1/2">
          <div
            @click="prevSlide"
            :class="['arrow__prev lg:-translate-x-13 -translate-x-5 -translate-y-7']"
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
            :class="['arrow__next xl:translate-x-13 translate-x-5 -translate-y-7']"
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
      </div>
      <Swiper
        class="swiper xl:h-[432px] h-auto rounded-[38px] w-full bg-[#F2F2F2] block"
        :space-between="size"
        :modules="modules"
        ref="swiperFreshPickRef"
        :slides-per-view="perView"
        :navigation="true"
        :loop="true"
        :pagination="{ clickable: true }"
        :centered-slides="true"
      >
        <SwiperSlide class="py-[48px] w-full" v-for="item in 5" :key="item"
          ><div
            class="inside h-full bg-[#648DE5] rounded-[28px] md:px-[56px] px-[12px] pt-[37px] pb-[15px] text-[#fff] flex flex-col"
          >
            <div class="flex-1 text-center">
              <img loading="lazy" src="/swiper_icon_voice.png" alt="" class="mx-auto" />
              <div class="text-[24px] leading-[24px] mt-[11px] font-medium">Пунин М.В.</div>
              <div class="text-[15px] leading-[23px] mt-[8px] font-medium mb-6">
                Пользователь находится на сайте 2 года
              </div>
            </div>
            <div
              class="flex-1 border-t-[1px] border-[#f3f3f3c2] pt-6 px-4 text-[#FCFBF3] text-center font-light"
            >
              Компания Ivideon выражает искреннюю благодарнсоть за сотрудничество интернет -
              агентству Looksmarkt. Благодаря вашей профессиональной работе мы смогли увеличить
              продажи наших продуктов и привлечь новых клиентов.
            </div>
          </div></SwiperSlide
        >
      </Swiper>
    </div>
    <div class="text-center">
      <button
        @click="emit('showPopup')"
        class="rounded-full md:mt-[36px] mt-[40px] bg-gradient-to-r from-[#648DE5] to-[#7DA7FF] text-[#fff] font-medium md:px-[66px] px-[28px] md:py-[36px] py-[18px] text-[22px] leading-[24px]"
      >
        Задать вопрос врачу
      </button>
    </div>
  </div>
</template>

<script setup>
import { computed, defineComponent, onMounted, ref, watch } from 'vue'
import { Pagination, Navigation } from 'swiper/modules'
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/pagination'
const size = ref(111)
const perView = ref(2)
const width = ref(window.innerWidth)
const emit = defineEmits(['showPopup'])

onMounted(() => {
  calcWidth()
})

const calcWidth = () => {
  if (window.innerWidth < 790) {
    size.value = 31
    perView.value = 1.3
  } else {
    size.value = 111
    perView.value = 2
  }
}
const modules = [Pagination, Navigation]

window.addEventListener('resize', (event) => {
  calcWidth()
})

watch(
  () => width.value,
  () => {
    calcWidth()
  }
)
const swiperFreshPickRef = ref(null)
const prevSlide = () => {
  swiperFreshPickRef.value?.$el.swiper.slidePrev()
}

const nextSlide = () => {
  swiperFreshPickRef.value?.$el.swiper.slideNext()
}
</script>
