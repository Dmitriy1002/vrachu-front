<script setup>
import IconMainFav from '@/components/icons/IconMainFav.vue'
import AskQuestion from '@/components/modals/AskQuestion.vue'
import { ref, onMounted, onUnmounted, watch } from 'vue'
import { onClickOutside } from '@vueuse/core'

const props = defineProps({
  isOpenPopup: {
    type: Boolean,
    default: false
  }
})
const target = ref(null)
watch(
  () => props.isOpenPopup,
  () => {
    toggle()
  }
)

const showPopup = ref(false)
const customDiv = ref()

onClickOutside(target, (event) => toggle())
const toggle = () => {
  showPopup.value = !showPopup.value
}
</script>
<template>
  <div class="main_banner md:mt-20 mt-0 relative overflow-hidden">
    <div v-if="showPopup" class="fixed top-0 z-50">
      <div class="w-screen min-h-screen overflow-auto bg-[#00000046] relative">
        <AskQuestion ref="target" class="absolute md:top-[150px] top-6 mx-auto pb-20">
          <template #closeIcon>
            <img loading="lazy" @click="toggle" class="cursor-pointer" src="/x.png" alt="" />
          </template>
        </AskQuestion>
      </div>
    </div>
    <div class="absolute top-0 h-[284px] w-full bg-gradient-to-t from-[#FFFFFF00] to-white"></div>
    <div class="2xl:w-[1418px] w-screen 2xl:px-0 px-5 mx-auto mt-[28px] relative">
      <div class="flex items-center justify-between w-full">
        <div class="md:mt-[136px] mt-[0px] md:mb-[111px] mb-[50px]">
          <div
            class="md:font-bold font-semibold xl:text-[70px] xl:leading-[72px] text-[40px] md:leading-[50px] leading-[42px]"
          >
            Консультация врача <br class="md:block hidden" />
            в режиме онлайн
            <IconMainFav class="inline rounded-full" />
          </div>
          <div class="text-[15px] mt-6">
            Пройди регистрацию в нашем <br class="md:hidden block" />
            сервисе и задай интересующий <br class="md:hidden block" />
            тебя вопрос нашим специалистам
          </div>
          <button
            @click="toggle"
            class="hover:bg-[#5086fa] rounded-full mt-[43px] bg-[#648DE5] text-[#fff] font-medium md:py-6 py-3 md:px-12 px-6 text-[15px]"
          >
            Задать вопрос врачу
          </button>
        </div>
      </div>
      <div class="flex gap-6">
        <img
          loading="lazy"
          src="/docktor-main.webp"
          class="absolute md:right-0 -right-10 bottom-0 xl:w-auto w-[320px] md:block hidden"
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.main_banner {
  background-image: url('/fon.webp');
  background-image: no-repeat;
}
</style>
