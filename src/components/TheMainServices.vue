<script setup>
import IconLogo from '@/components/icons/IconLogo.vue'
import IconSearch from '@/components/icons/IconSearch.vue'
import IconMainFav from '@/components/icons/IconMainFav.vue'
import TheMainServiceFree from '@/components/TheMainServiceFree.vue'
import TheMainServicePayment from '@/components/TheMainServicePayment.vue'
import TheMainServiceConsultation from '@/components/TheMainServiceConsultation.vue'
</script>
<template>
  <div class="relative mt-[72px]">
    <div class="text-[31px] leading-[36px] font-medium">Возможности сервиса</div>
    <div
      class="md:mt-[48px] mt-5 flex gap-[22px] justify-between items-center xl:flex-row flex-col"
    >
      <div class="xl:h-[540px] h-fit w-full">
        <TheMainServiceFree class=""></TheMainServiceFree>
      </div>
      <div class="xl:h-[540px] h-fit w-full">
        <TheMainServicePayment class=""></TheMainServicePayment>
      </div>
    </div>
    <div class="mt-[22px]">
      <div class="xl:h-[540px] h-fit">
        <TheMainServiceConsultation class=""></TheMainServiceConsultation>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
