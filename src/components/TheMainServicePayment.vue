<script setup>
import IconLogo from '@/components/icons/IconLogo.vue'
import IconSearch from '@/components/icons/IconSearch.vue'
import IconMainFav from '@/components/icons/IconMainFav.vue'
import TheMainNavbar from '@/components/TheMainNavbar.vue'
</script>
<template>
  <div class="module relative h-full">
    <svg width="0" height="0">
      <linearGradient id="grad" x1="1" x2="1" y1="0" y2="1">
        <stop offset="0" />
        <stop offset="1" />
      </linearGradient>
      <symbol id="border" overflow="visible">
        <rect width="100%" height="100%" rx="8px" ry="8px" />
      </symbol>
    </svg>
    <svg class="module-border"><use href="#border" /></svg>

    <!-- <div class="absolute top-0 h-[284px] w-full bg-gradient-to-t from-[#FFFFFF00] to-white"></div> -->
    <div class="mx-auto h-full relative">
      <div class="flex h-full items-start justify-between flex-col w-full pt-[26px] pl-[31px]">
        <div class="">
          <div class="font-semibold text-[30px] leading-[30px]">
            <span> Консилиум: </span>
            <br />
            <span class="text-[#648DE5]"> платный режим </span>
          </div>
          <div class="text-[15px] mt-[18px] ml-5">
            <ul class="list-disc text-[16px] leading-[24px] lg:w-[370px] md:pr-0 pr-3">
              <li>Моментальная публикация</li>
              <li>Гарантия получения ответов нескольких врачей</li>
              <li>Первые ответы в среднем в течение 15 минут</li>
              <li>Возможность загрузить сканы или фотографии анализов</li>
            </ul>
          </div>
        </div>
        <div>
          <div
            class="text-[35px] leading-[28px] font-bold md:mt-0 mt-6"
            style="
              background-image: linear-gradient(90deg, #2fcc59, #14b840);
              background-size: 100%;
              -webkit-background-clip: text;
              -moz-background-clip: text;
              -webkit-text-fill-color: transparent;
              -moz-text-fill-color: transparent;
            "
          >
            От 400 ₽
          </div>
          <div
            class="mt-[18px] text-[15px] font-light leading-[24px] text-[#7F7F7F] md:w-[320px] md:pr-0 pr-3"
          >
            Вы можете назначить вознаграждение больше. Чем выше вознаграждение — тем больше врачей
            ответит на ваш вопрос
          </div>
          <button
            class="rounded-full my-[24px] bg-[#648DE5] text-[#fff] font-medium py-6 px-12 text-[15px]"
          >
            Задать платный вопрос
          </button>
        </div>
      </div>
      <div class="flex gap-6">
        <img
          loading="lazy"
          src="/service_payment.webp"
          class="absolute right-0 bottom-0 md:block hidden"
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.module {
  position: relative;
}
.module-border {
  position: absolute;
  overflow: visible;
  left: 0;
  width: 100%;
  top: 0;
  height: 100%;
  fill: none;
  stroke: url(#grad);
  stroke-width: 1px;
}
#grad stop:nth-child(1) {
  stop-color: #648de5;
}
#grad stop:nth-child(2) {
  stop-color: #374e7f1e;
}
</style>
