<template>
  <div class="mt-[115px] mb-[50px]">
    <div class="text-[31px] leading-[36px] font-medium">Популярные публикации</div>
    <div class="md:mt-[82px] mt-[32px] flex gap-[100px] xl:flex-row flex-col">
      <div class="xl:w-[500px] w-full">
        <div class="xl:h-[500px] w-full aspect-square bg-[#F2F2F2]"></div>
        <div class="text-[#000000b8] text-[15x] leading-[24px] mt-[29px]">22.02.2024 13:46</div>
        <div class="text-[22px] hover:underline cursor-pointer leading-[24px] mt-[6px]">
          Сирдалуд: инструкция по применению, от чего помогает, аналоги препарата, отзывы
        </div>
        <button
          class="rounded-full mt-[21px] bg-[#648DE5] hover:bg-[#5588f5] text-[#fff] font-medium py-[17px] px-[51px] text-[15px] leading-6"
        >
          Читать
        </button>
      </div>
      <div class="">
        <div class="flex md:gap-[34px] gap-[16px] mb-[21px]" v-for="item in 3" :key="item">
          <div class="min-w-[153px] h-[153px] bg-[#F2F2F2]"></div>
          <div class="flex flex-col justify-between items-start">
            <div>
              <div class="text-[#000000b8] text-[15x] leading-[24px]">22.02.2024 13:46</div>
              <div
                class="md:text-[18px] text-[15px] md:leading-[24px] mt-[6px] hover:underline cursor-pointer"
              >
                Сирдалуд: инструкция по применению, от чего помогает, аналоги препарата, отзывы
              </div>
            </div>
            <button
              class="rounded-full md:mt-0 mt-3 bg-[#648DE5] hover:bg-[#5588f5] text-[#fff] font-medium py-[11px] px-[40px] text-[15px] leading-6"
            >
              Читать
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>
