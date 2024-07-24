<script setup>
import IconLogo from '@/components/icons/IconLogo.vue'
import IconSearch from '@/components/icons/IconSearch.vue'
import TheMainNavbar from '@/components/TheMainNavbar.vue'
import TheMainNavbarMobile from '@/components/TheMainNavbarMobile.vue'
</script>
<template>
  <div>
    <div class="2xl:w-[1418px] w-screen 2xl:px-0 px-5 mx-auto mt-[28px]">
      <div class="flex items-center justify-between w-full">
        <div class="flex items-center divide-x-[1px] divide-[#E6E6E6]">
          <IconLogo class="md:mr-[24px] md:w-auto w-30 mt-1"></IconLogo>
          <div class="text-[15px] pl-[24px] leading-5 2xl:flex hidden">
            Задай вопрос врачу онлайн и <br />
            получи ответ мгновенно
          </div>
        </div>
        <div class="flex gap-6">
          <div class="w-[456px] 2xl:flex hidden p-[12px] border rounded-full border-[#E6E6E6]">
            <IconSearch class="mx-[12px] block"></IconSearch>
            <input
              class="outline-none placeholder:text-[#7F7F7F] placeholder:text-[15px] placeholder:leading-6"
              placeholder="Введите запрос"
            />
          </div>
          <div class="flex gap-2">
            <button class="rounded-full bg-[#F2F2F2] md:py-3 py-2 md:px-6 px-4 text-[15px]">
              Вход
            </button>
            <button
              class="rounded-full bg-[#648DE5] text-[#fff] font-medium md:py-3 py-2 md:px-6 px-4 text-[15px]"
            >
              Регистрация
            </button>
          </div>
        </div>
      </div>
      <TheMainNavbar class="hidden md:block"></TheMainNavbar>
      <TheMainNavbarMobile class="md:hidden block"></TheMainNavbarMobile>
    </div>
  </div>
</template>

<style></style>
