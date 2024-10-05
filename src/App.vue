<script>
import AboutUs from './components/AboutUs.vue';
import FirstScreen from './components/FirstScreen.vue';
import GroupInfo from './components/GroupInfo.vue';
import HomepageHeader from './components/HomepageHeader.vue';
import HowtoJoinUs from './components/HowtoJoinUs.vue';
import MembersTalk from './components/MembersTalk.vue';
import OurProducts from './components/OurProducts.vue';
import WhyJoinUs from './components/WhyJoinUs.vue';

export default {
  components: {
    HomepageHeader,
    FirstScreen,
    AboutUs,
    OurProducts,
    GroupInfo,
    WhyJoinUs,
    MembersTalk,
    HowtoJoinUs
  }
}
</script>

<template>
  <header>
    <HomepageHeader />
  </header>

  <main class="overflow-hidden">
    <FirstScreen />
    <div class="mx-auto max-w-[1280px] pt-12 px-4 mt-3 py-3 space-y-8">
      <AboutUs />
      <OurProducts />
      <GroupInfo />
      <WhyJoinUs />
      <MembersTalk />
      <HowtoJoinUs />
    </div>
  </main>

</template>

<style></style>
