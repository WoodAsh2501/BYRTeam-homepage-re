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
  },
  data() {
    return {
      scrollIntoMain: false,
    }
  },
  methods: {
    headerScroll() {
      this.scrollIntoMain = window.scrollY > window.innerHeight ? true : false
    },
  },
  mounted() {
    window.addEventListener('scroll', this.headerScroll)
  }
}
</script>

<template>
  <header>
    <HomepageHeader :scrollIntoMain />
  </header>

  <main class="overflow-hidden">
    <FirstScreen />
    <div id="mainDiv" class="mx-auto max-w-[1200px] pt-12 px-6 mt-3 py-3 space-y-8">
      <AboutUs />
      <OurProducts />
      <GroupInfo />
      <WhyJoinUs />
      <MembersTalk />
      <HowtoJoinUs />
    </div>
  </main>
  <footer class="mt-20 py-6 text-center text-sm text-[#999]">
    <div>2003 ~ 2024 © 北邮人团队 BYR TEAM</div>
    <div>Design &amp; Code with <span class="text-[#ff5a79]">❤</span></div>
  </footer>
</template>

<style>
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translate3d(0, -5%, 0);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

main > *{
  animation-name: fadeIn;
  animation-duration: 1.3s;
  animation-fill-mode: both;
}
</style>
