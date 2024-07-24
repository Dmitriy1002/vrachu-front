<script setup>
import IconLogo from '@/components/icons/IconLogoFooter.vue'
import IconSearch from '@/components/icons/IconSearch.vue'
import IconMainFav from '@/components/icons/IconMainFav.vue'
import TheMainNavbar from '@/components/TheMainNavbar.vue'

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}
</script>
<template>
  <div class="bg-gradient-to-br from-[#648DE5] to-[#A5C1FF] text-white">
    <div
      class="2xl:ml-[calc((100vw-1418px)/2)] ml-0 xl:mr-[86px] mr-0 2xl:w-auto w-full 2xl:px-0 px-5 xl:pt-[91px] pt-[60px] pb-[70px] relative"
    >
      <div class="w-full flex justify-between xl:flex-row flex-col">
        <div class="flex justify-between flex-grow md:flex-row flex-col gap-4">
          <div class="xl:w-[304px] font-medium">
            <IconLogo></IconLogo>
            <div class="mt-[29px] text-[34px] md:pb-4 pb-1 border-b">Свяжись с нами!</div>
            <div class="flex md:mt-[74px] mt-[20px] gap-5">
              <div>
                <svg
                  width="25"
                  height="25"
                  viewBox="0 0 25 25"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M20.7812 21.875C18.6111 21.875 16.467 21.4021 14.349 20.4562C12.2309 19.5104 10.3038 18.1691 8.56771 16.4323C6.8316 14.6962 5.49062 12.7691 4.54479 10.651C3.59896 8.53299 3.12569 6.38889 3.125 4.21875C3.125 3.90625 3.22917 3.64583 3.4375 3.4375C3.64583 3.22917 3.90625 3.125 4.21875 3.125H8.4375C8.68056 3.125 8.89757 3.20764 9.08854 3.37292C9.27951 3.53819 9.39236 3.73333 9.42708 3.95833L10.1042 7.60417C10.1389 7.88194 10.1302 8.11632 10.0781 8.30729C10.026 8.49826 9.93055 8.66319 9.79167 8.80208L7.26562 11.3542C7.61285 11.9965 8.025 12.617 8.50208 13.2156C8.97917 13.8142 9.50451 14.3917 10.0781 14.9479C10.6163 15.4861 11.1806 15.9854 11.7708 16.4458C12.3611 16.9062 12.9861 17.3271 13.6458 17.7083L16.0937 15.2604C16.25 15.1042 16.4542 14.9872 16.7062 14.9094C16.9583 14.8316 17.2056 14.8097 17.4479 14.8438L21.0417 15.5729C21.2847 15.6424 21.4844 15.7684 21.6406 15.951C21.7969 16.1337 21.875 16.3375 21.875 16.5625V20.7812C21.875 21.0938 21.7708 21.3542 21.5625 21.5625C21.3542 21.7708 21.0938 21.875 20.7812 21.875Z"
                    fill="#FCFBF3"
                  />
                </svg>
              </div>
              <div>+7 111 111-11-11</div>
            </div>
            <div class="flex mt-[21px] gap-5">
              <div>
                <svg
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M16 19.0002L21 14.0002L16 9.00024"
                    stroke="#FCFBF3"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                  <path
                    d="M21 14.0005L13 14.0005C7.477 14.0005 3 9.52349 3 4.00049L3 3.00049"
                    stroke="#FCFBF3"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </svg>
              </div>
              <div class="underline">vrach24.com</div>
            </div>
          </div>
          <div class="w-[273px]">
            <div class="text-[24px] font-medium">Меню</div>
            <div class="mt-[37px]">
              <div class="hover:text-[#ffffffb6] cursor-pointer pb-[7px] border-b mb-[21px]">
                Главная
              </div>
              <div class="hover:text-[#ffffffb6] cursor-pointer pb-[7px] border-b mb-[21px]">
                Задать вопрос врачу
              </div>
              <div class="hover:text-[#ffffffb6] cursor-pointer pb-[7px] border-b mb-[21px]">
                Консультация
              </div>
              <div class="hover:text-[#ffffffb6] cursor-pointer pb-[7px] border-b mb-[21px]">
                Врачи
              </div>
              <div class="hover:text-[#ffffffb6] cursor-pointer pb-[7px] border-b mb-[21px]">
                Статьи
              </div>
              <div class="hover:text-[#ffffffb6] cursor-pointer pb-[7px] border-b mb-[21px]">
                Помощь
              </div>
            </div>
          </div>
          <div class="2xl:w-[455px] w-[300px]">
            <div class="text-[24px] font-medium">Важное</div>
            <div class="mt-[37px]">
              <div
                class="pb-[7px] border-b mb-[21px] cursor-pointer hover:text-[#fff] w-[260px] text-nowrap"
              >
                Политика обработки персональных данных
              </div>
              <div
                class="pb-[7px] border-b mb-[21px] w-[260px] cursor-pointer hover:text-[#ffffffbd]"
              >
                Политика конфиденциальности
              </div>
            </div>
          </div>
        </div>
        <div class="flex flex-col justify-between 2xl:ml-[85px] ml-0">
          <div class="">
            <img
              @click="scrollToTop"
              loading="lazy"
              class="ml-auto cursor-pointer xl:mr-0 mr-5 xl:mb-0 mb-5 xl:w-auto w-20"
              src="/footer-top.png"
              alt=""
            />
          </div>
          <div class="flex gap-[13px]">
            <img loading="lazy" class="cursor-pointer" src="/footer_youtube.png" alt="" />
            <img loading="lazy" class="cursor-pointer" src="/footer_tg.png" alt="" />
            <img loading="lazy" class="cursor-pointer" src="/footer_vk.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
