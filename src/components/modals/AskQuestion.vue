<script setup>
import { ref } from 'vue'

const sections = ref([
  { name: 'blabla1' },
  { name: 'blabla2' },
  { name: 'blabla3' },
  { name: 'blabla4' }
])
const isSectonOpen = ref(false)
const selectedItem = ref(null)
const selectItem = (e) => {
  isSectonOpen.value = false
  selectedItem.value = e
}
</script>
<template>
  <div class="xl:w-[606px] w-[calc(100vw-40px)] relative pb-27">
    <div class="bg-[#ECECEC] rounded-[29px] h-auto md:px-[35px] px-[16px]">
      <div class="absolute top-[26px] right-[30px] md:w-auto w-[30px]">
        <slot name="closeIcon" />
      </div>
      <div class="absolute top-0 -translate-y-1/2 right-1/2 translate-x-1/2 md:block hidden">
        <img loading="lazy" src="/popup_question.png" alt="" />
      </div>
      <div class="text-[41px] leading-[26px] md:pt-[210px] pt-[70px] font-bold text-center">
        Задать вопрос <span class="text-[#EA246C]">врачу</span>
      </div>
      <div class="md:mt-[15px] mt-6 w-full mx-auto">
        <div class="w-[91px] md:mb-2 mb-1 rounded-full h-[3px] mx-auto bg-[#EA246C]"></div>
        <div class="w-[70px] md:mb-2 mb-1 rounded-full h-[3px] mx-auto bg-[#ea246db1]"></div>
        <div class="w-[44px] md:mb-2 mb-1 rounded-full h-[3px] mx-auto bg-[#ea246d67]"></div>
      </div>
      <div class="mt-[52px]">
        <div
          @click="isSectonOpen = !isSectonOpen"
          class="p-4 rounded-full bg-[#BFBFBF] flex justify-between relative"
        >
          <div class="text-[15px] lading-[24px] font-medium text-white">
            <div>{{ !selectedItem ? 'Выберите раздел медицины' : selectedItem.name }}</div>
          </div>
          <div>
            <svg
              width="22"
              height="21"
              viewBox="0 0 22 21"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M18.333 7.875L10.9997 14.875L3.66634 7.875L5.49967 6.125L10.9997 11.375L16.4997 6.125L18.333 7.875Z"
                fill="white"
              />
            </svg>
          </div>
        </div>
        <Transition name="fade">
          <div v-if="isSectonOpen" class="bg-[#adadad] rounded-2xl mt-3 w-[calc(100%-0px)] p-4">
            <div v-for="section in sections" :key="section.name" class="flex items-center mb-2">
              <input
                @click.stop="selectItem(section)"
                :id="section.name"
                type="radio"
                name="section"
                class="h-[24px] w-[24px] mr-[5px] cursor-pointer"
              />
              <label :for="section.name" class="text-[15px] lading-[24px] font-medium text-white">
                {{ section.name }}
              </label>
            </div>
          </div>
        </Transition>

        <div class="mt-[19px] p-4 rounded-full bg-[#BFBFBF]">
          <input
            class="text-[15px] lading-[24px] font-medium text-white bg-[#BFBFBF] placeholder:text-white w-full outline-none"
            placeholder="Краткий заголовок вопроса"
          />
        </div>
        <div class="text-[#0000003d] pl-4 pt-[2px]">Например: “Почему болит живот?”</div>
        <div class="mt-[34px] p-4 rounded-[30px] bg-[#BFBFBF]">
          <textarea
            class="text-[15px] lading-[24px] font-medium text-white bg-[#BFBFBF] placeholder:text-white w-full outline-none"
            placeholder="Ваш вопрос врачу, постарайтесь описать свою проблему наиболее детально"
          />
        </div>
        <div class="text-[#0000003d] pl-4 pt-[2px]">Необходимо ввести не менее 100 символов</div>

        <div class="mt-[19px] p-4 rounded-full bg-[#BFBFBF]">
          <input
            class="text-[15px] lading-[24px] font-medium text-white bg-[#BFBFBF] placeholder:text-white w-full outline-none"
            placeholder="Задайте ключевые слова через запятую"
          />
        </div>
        <div class="text-[#0000003d] pl-4 pt-[2px]">Например: зубы, живот, сердце</div>
      </div>
      <div class="mt-6 flex justify-between items-center pb-[18px] gap-6">
        <div class="flex gap-[13px] flex-grow items-center">
          <input type="checkbox" name="section" class="h-[34px] w-[34px] mr-[5px] cursor-pointer" />
          <div class="text-[#0000003a] text-[10px] leading-[14px]">
            Я ознакомился с лицензионным <br />
            соглашением и политикой обработки данных
          </div>
        </div>
        <button
          class="py-3 md:px-[37px] px-4 text-white rounded-full text-[15px] font-medium bg-[#EA246C]"
        >
          Отправить
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
