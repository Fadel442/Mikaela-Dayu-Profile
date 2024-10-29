<template>
    <main>
        <MainIntro />
        <AboutMe />
        <TitleSec section="SKILLS" />
        <SkillCards />
        <TitleSec section="AWARDS" />
        <MyAwards />
        <FooterV />
    </main>
</template>

<script>
import MainIntro from '../../components/komponen/MainIntro.vue'
import AboutMe from '../../components/komponen/AboutMe.vue'
import TitleSec from '../../components/komponen/TitleSec.vue'
import SkillCards from '../../components/komponen/SkillCards.vue'
import MyAwards from '../../components/komponen/MyAwards.vue'
import FooterV from '../../components/komponen/FooterV.vue'

export default {
    components: {MainIntro, AboutMe, TitleSec, SkillCards, MyAwards, FooterV }
}
</script>
