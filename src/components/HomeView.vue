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
</script>

<template>
  <main>
    <TheMainBanner></TheMainBanner>
    <div class="w-[1418px] mx-auto">
      <TheMainShowcase></TheMainShowcase>
      <TheMainTable></TheMainTable>
      <TheMainServices></TheMainServices>
      <TheMainExServices></TheMainExServices>
      <TheMainAwwards></TheMainAwwards>
      <TheMainSwiperCertificate></TheMainSwiperCertificate>
      <TheMainSwiperUsersVoice></TheMainSwiperUsersVoice>
      <TheMainFamousBlogs></TheMainFamousBlogs>
    </div>
    <TheFooter></TheFooter>
  </main>
</template>
