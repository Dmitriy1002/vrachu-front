<script setup>
import TheMainBanner from '../components/TheMainBanner.vue'
import TheMainShowcase from '../components/TheMainShowcase.vue'
import TheMainTable from '../components/TheMainTable.vue'
import TheMainServices from '../components/TheMainServices.vue'
import TheMainExServices from '../components/TheMainExServices.vue'
import TheMainAwwards from '../components/TheMainAwwards.vue'
import TheMainSwiperCertificate from '../components/TheMainSwiperCertificate.vue'
import TheMainSwiperUsersVoice from '../components/TheMainSwiperUsersVoice.vue'
import TheMainFamousBlogs from '../components/TheMainFamousBlogs.vue'
import TheFooter from '../components/TheFooter.vue'
import { ref } from 'vue'

const isOpenPopup = ref(false)

const incomeSignal = () => {
  console.log('hgg')
  isOpenPopup.value = !isOpenPopup.value
}
</script>

<template>
  <main>
    <TheMainBanner :isOpenPopup="isOpenPopup"></TheMainBanner>
    <div class="2xl:w-[1418px] w-screen 2xl:px-0 px-5 mx-auto overflow-hidden">
      <TheMainShowcase></TheMainShowcase>
      <TheMainTable></TheMainTable>
      <TheMainServices></TheMainServices>
      <TheMainExServices></TheMainExServices>
      <TheMainAwwards></TheMainAwwards>
      <TheMainSwiperCertificate></TheMainSwiperCertificate>
      <TheMainSwiperUsersVoice @showPopup="incomeSignal"></TheMainSwiperUsersVoice>
      <TheMainFamousBlogs></TheMainFamousBlogs>
    </div>
  </main>
</template>
