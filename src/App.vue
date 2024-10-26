<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Navi from './components/nav/Navi.vue'
import MainIntro from './components/komponen/MainIntro.vue'
import AboutMe from './components/komponen/AboutMe.vue'
import TitleSec from './components/komponen/TitleSec.vue'
import SkillCards from './components/komponen/SkillCards.vue'
import MyAwards from './components/komponen/MyAwards.vue'
import FooterV from './components/komponen/FooterV.vue'
</script>

<template>
  <header>
    <Navi />
  </header>
  <main>
    <MainIntro />
    <AboutMe />
    <TitleSec section="SKILLS" />
    <SkillCards />
    <TitleSec section="AWARDS" />
    <MyAwards />
    <FooterV />
  </main>
  <RouterView />
</template>

<script>
export default {
  data() {
    components: { Navi, MainIntro, AboutMe, TitleSec, SkillCards, MyAwards, FooterV }
    return {

    }
  },
}
</script>

<style scoped></style>
