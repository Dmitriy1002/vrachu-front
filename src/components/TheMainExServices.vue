<script setup>
import IconLogo from '@/components/icons/IconLogo.vue'
import IconSearch from '@/components/icons/IconSearch.vue'
import IconMainFav from '@/components/icons/IconMainFav.vue'
import TheMainServiceFree from '@/components/TheMainServiceFree.vue'
import TheMainServicePayment from '@/components/TheMainServicePayment.vue'
import TheMainServiceConsultation from '@/components/TheMainServiceConsultation.vue'
</script>
<template>
  <div class="relative xl:mt-[88px] mt-[38px]">
    <div class="text-[31px] leading-[36px] font-medium">Дополнительные услуги</div>
    <div class="mt-[54px] flex gap-[27px] justify-between xl:flex-row flex-col">
      <div class="flex-1 h-[294px]">
        <div
          class="relative h-full border bg-gradient-to-br from-[#3AC7D5] to-[#30E8FF] rounded-[8px]"
        >
          <!-- <div class="absolute top-0 h-[284px] w-full bg-gradient-to-t from-[#FFFFFF00] to-white"></div> -->
          <div class="mx-auto h-full relative">
            <div
              class="flex h-full items-start justify-between flex-col w-full pt-[26px] pl-[31px]"
            >
              <div class="">
                <div class="text-[30px] leading-[34px] font-medium">
                  <span> Консультация </span>
                  <br />
                  <span class="text-[#FF4B8C]"> дежурного врача </span>
                </div>
                <div
                  class="mt-[14px] text-[15px] font-light leading-[24px] text-[#000000B2] w-[282px]"
                >
                  Опытный дежурный врач свяжется с вами в течении 3-х минут, проведет осмотр и даст
                  рекомендации
                </div>
              </div>
              <div>
                <div class="flex gap-[13px] items-center">
                  <button
                    class="rounded-full my-[24px] bg-[#FF4B8C] hover:bg-[#f83b81] text-[#fff] font-medium py-3 px-8.5 text-[13px]"
                  >
                    Перейти
                  </button>
                  <div class="text-[15px] leading-[28px] font-medium">От 1500 ₽</div>
                </div>
              </div>
            </div>
            <div class="flex gap-6">
              <img
                loading="lazy"
                src="/ex_1.png"
                class="absolute right-0 bottom-0 md:w-auto w-30"
                alt=""
              />
            </div>
          </div>
        </div>
      </div>
      <div class="flex-1 h-[294px]">
        <div
          class="relative h-full border bg-gradient-to-br from-[#b8da90] to-[#C7DFAB] rounded-[8px]"
        >
          <!-- <div class="absolute top-0 h-[284px] w-full bg-gradient-to-t from-[#FFFFFF00] to-white"></div> -->
          <div class="mx-auto h-full relative">
            <div
              class="flex h-full items-start justify-between flex-col w-full pt-[26px] pl-[31px]"
            >
              <div class="">
                <div class="text-[30px] leading-[34px] font-medium">
                  <span> Психологическая </span>
                  <br />
                  <span class="text-[#FF4B8C]"> помощь </span>
                </div>
                <div
                  class="mt-[14px] text-[15px] font-light leading-[24px] text-[#000000B2] w-[182px]"
                >
                  Консультация с опытным психологом
                </div>
              </div>
              <div>
                <div class="flex gap-[13px] items-center">
                  <button
                    class="rounded-full my-[24px] bg-[#FF4B8C] hover:bg-[#f83b81] text-[#fff] font-medium py-3 px-8.5 text-[13px]"
                  >
                    Перейти
                  </button>
                  <div class="text-[15px] leading-[28px] font-medium">От 2000 ₽</div>
                </div>
              </div>
            </div>
            <div class="flex gap-6">
              <img
                loading="lazy"
                src="/ex_2.png"
                class="absolute right-0 bottom-0 md:w-auto w-30"
                alt=""
              />
            </div>
          </div>
        </div>
      </div>
      <div class="flex-1 h-[294px]">
        <div
          class="relative h-full border bg-gradient-to-br from-[#a4bdfb] to-[#5b85f1] rounded-[8px]"
        >
          <!-- <div class="absolute top-0 h-[284px] w-full bg-gradient-to-t from-[#FFFFFF00] to-white"></div> -->
          <div class="mx-auto h-full relative">
            <div
              class="flex h-full items-start justify-between flex-col w-full pt-[26px] pl-[31px]"
            >
              <div class="">
                <div class="text-[30px] leading-[34px] font-medium">
                  <span> Абонемент на </span>
                  <br />
                  <span class="text-[#FF4B8C]">
                    медицинское <br />
                    обслуживание
                  </span>
                </div>
                <div
                  class="mt-[14px] text-[15px] font-light leading-[24px] text-[#000000B2] w-[182px]"
                >
                  Врач будет на связи круглосуточно!
                </div>
              </div>
              <div>
                <div class="flex gap-[13px] items-center">
                  <button
                    class="rounded-full my-[24px] bg-[#FF4B8C] hover:bg-[#f83b81] text-[#fff] font-medium py-3 px-8.5 text-[13px]"
                  >
                    Перейти
                  </button>
                  <div class="text-[15px] leading-[28px] font-medium">От 200 ₽</div>
                </div>
              </div>
            </div>
            <div class="flex gap-6">
              <img
                loading="lazy"
                src="/ex_3.png"
                class="absolute right-0 bottom-0 md:w-auto w-30"
                alt=""
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
