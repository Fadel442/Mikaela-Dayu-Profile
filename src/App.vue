<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Navi from './components/nav/Navi.vue'
// import MainIntro from './components/komponen/MainIntro.vue'
// import AboutMe from './components/komponen/AboutMe.vue'
// import TitleSec from './components/komponen/TitleSec.vue'
// import SkillCards from './components/komponen/SkillCards.vue'
// import MyAwards from './components/komponen/MyAwards.vue'
// import FooterV from './components/komponen/FooterV.vue'
</script>

<template>
  <header>
    <Navi />
  </header>
</template>

<script>
export default {
  components: { Navi },
  data() {
    return {

    }
  },
}
</script>

<style scoped>
header {
  margin: 0 100px;
}
main {
  margin: 0 100px;
}

@media (max-width: 400px)
{
  header {
    margin: 0;
  }
  main {
    margin: 0;
  }
}

@media (max-width: 480px)
{
  header {
    margin: 0;
  }
  main {
    margin: 0;
  }
}
</style>
