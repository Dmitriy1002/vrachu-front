<script setup>
import IconLogo from '@/components/icons/IconLogo.vue'
import IconSearch from '@/components/icons/IconSearch.vue'
import IconMainFav from '@/components/icons/IconMainFav.vue'
import TheMainServiceFree from '@/components/TheMainServiceFree.vue'
import TheMainServicePayment from '@/components/TheMainServicePayment.vue'
import TheMainServiceConsultation from '@/components/TheMainServiceConsultation.vue'
</script>
<template>
  <div class="relative mt-[116px]">
    <div class="flex gap-[27px] justify-between xl:flex-row flex-col">
      <div class="xl:text-start text-center">
        <div class="text-[31px] leading-[36px] font-medium">
          Квалифицированные <br />
          консультации врачей
        </div>
        <div class="text-[15px] leading-[24px] font-light text-[#7F7F7F] mt-[24px]">
          Сервис несёт полную моральную и юридическую <br />
          ответственность за качество консультаций
        </div>
      </div>
      <div class="">
        <div class="flex md:gap-[24px] gap-4">
          <div class="md:w-[296px]">
            <img loading="lazy" class="mx-auto" src="/awward_1.png" alt="" />
            <div class="mt-[24px] text-center md:text-base text-[12px]">
              Большой выбор специалистов: от <br class="md:block hidden" />
              гинеколога до педиатра
            </div>
          </div>
          <div class="md:w-[296px]">
            <img loading="lazy" class="mx-auto" src="/awward_2.png" alt="" />
            <div class="mt-[24px] text-center md:text-base text-[12px]">
              Медицинское образование <br class="md:block hidden" />
              проверено администрацией сайта
            </div>
          </div>
          <div class="md:w-[296px]">
            <img loading="lazy" class="mx-auto" src="/awward_3.png" alt="" />
            <div class="mt-[24px] text-center md:text-base text-[12px]">
              Внедрена система рейтинга оценки <br class="md:block hidden" />
              врачей по отзывам пациентов
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
