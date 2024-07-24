<script setup>
import IconLogo from '@/components/icons/IconLogo.vue'
import IconSearch from '@/components/icons/IconSearch.vue'
import IconMainFav from '@/components/icons/IconMainFav.vue'
import TheMainNavbar from '@/components/TheMainNavbar.vue'
import { ref } from 'vue'

const datas = ref([
  {
    name: 'Повышен билирубин',
    count: 0,
    who: 'Мария, Зеленоград',
    price: '900 ₽',
    time: '12 минут'
  },
  {
    name: 'ОАК ребёнка',
    count: 5,
    who: 'Софья',
    price: '600 ₽',
    time: '13 минут'
  },
  {
    name: 'Грыжа со смещением позвонка',
    count: 0,
    who: 'Елена, Иркутск',
    price: '1 000 ₽',
    time: '30 минут'
  },
  {
    name: 'АД перестал работать на полпути. Что делать?',
    count: 16,
    who: 'Софья',
    price: '700 ₽',
    time: '1 час'
  },
  {
    name: 'Сыпь у новорождённого',
    count: 21,
    who: 'Елена, Иркутск',
    price: '400 ₽',
    time: '1 час'
  }
])

const addItem = () => {
  datas.value.push({
    name: 'АД перестал работать на полпути. Что делать?',
    count: 16,
    who: 'Софья',
    price: '700 ₽',
    time: '1 час'
  })
}
</script>
<template>
  <div class="relative md:mt-[123px] mt-[60px] flex justify-between gap-[33px]">
    <div class="flex-1">
      <div
        class="flex justify-between items-start pb-[29px] border-b border-[#E6E6E6] md:flex-row flex-col"
      >
        <div class="w-fit">
          <div class="md:text-[31px] w-fit text-[24px] md:leading-9 font-medium">
            Консультации врачей
          </div>
          <div class="text-[20px] leading-[24px] font-medium mt-3">
            <span class="text-[#9CCF26]">2 572 </span>
            <span class="text-[15px] leading-6 font-light text-[#7F7F7F]"> вопроса за сутки </span>
          </div>
        </div>
        <div class="flex gap-2 mt-[6px] flex-shrink-0">
          <button
            class="rounded-full border hover:border-[#648DE5] border-[#E6E6E6] py-3 md:px-6 px-3 text-[15px] flex items-center"
          >
            <img src="/fire.png" loading="lazy" class="inline md:mr-3 mr-1" alt="" /> Платные
          </button>
          <button
            class="rounded-full text-[#7F7F7F] border hover:border-[#648DE5] border-[#E6E6E6] font-medium py-3 md:px-6 px-3 text-[15px] leading-[24px]"
          >
            Бесплатные
          </button>
        </div>
      </div>
      <div>
        <div
          v-for="data in datas"
          :key="data"
          class="py-[24px] flex justify-between md:gap-0 gap-2 items-start border-b border-[#E6E6E6]"
        >
          <div class="md:flex-1 flex-1">
            <div
              class="md:text-[23px] text-[17px] leading-[28px] font-medium cursor-pointer hover:underline md:mb-0 mb-5"
            >
              {{ data.name }}
              <span
                :class="
                  data.count > 0 ? 'bg-[#9CCF26] text-[#FFFFFF]' : 'bg-[#F2F2F2] text-[#7F7F7F]'
                "
                class="text-[15px] inline-block leading-6 font-medium rounded-full ml-3 px-3"
              >
                {{ data.count }} ответов
              </span>
            </div>
            <div class="text-[15px] leading-6 font-light text-[#7F7F7F]">Софья</div>
          </div>
          <div class="flex gap-6 md:flex-row flex-col">
            <div
              class="rounded-full py-3 md:w-[156px] w-[90px] flex items-center text-[#9CCF26] text-[23px] leading-7 font-medium text-center"
            >
              {{ data.price }}
            </div>
            <div
              class="rounded-full text-[#7F7F7F] md:w-[156px] text-nowrap mr-1 w-[110px] font-light py-3 leading-[24px] text-end"
            >
              {{ data.time }} назад
            </div>
          </div>
        </div>
      </div>
      <div class="text-center">
        <button
          @click="addItem"
          class="mt-6 mx-auto font-medium px-6 py-3 text-[15px] leading-6 text-white bg-[#648DE5] rounded-[8px]"
        >
          Показать ещё
        </button>
      </div>
    </div>
    <div class="mt-[8px] relative xl:block hidden">
      <div class="text-[25px] leading-[34px] font-semibold absolute top-9 left-6 text-[#FFFFFF]">
        Индивидуальная консультация от 500 рублей
      </div>
      <img class="" loading="lazy" src="/table-banner.webp" alt="" />
    </div>
  </div>
</template>

<style scoped></style>
