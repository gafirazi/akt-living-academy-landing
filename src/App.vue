<template>
  <div id="app">
    <NavBar />
    <LandingSection />
    <ProblemSection />
    <RiskSection />
    <SolutionSection />
    <SellingPointSection />
    <SkillsSection />
    <ClassSection />
    <StatisticSection />
    <ContactUsSection />
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
import LandingSection from '@/components/LandingSection.vue'
import ProblemSection from '@/components/ProblemSection.vue'
import RiskSection from '@/components/RiskSection.vue'
import SolutionSection from '@/components/SolutionSection.vue'
import SellingPointSection from '@/components/SellingPointSection.vue'
import SkillsSection from '@/components/SkillsSection.vue'
import ClassSection from '@/components/ClassSection.vue'
import StatisticSection from '@/components/StatisticSection.vue'
import ContactUsSection from '@/components/ContactUsSection.vue'

export default {
  name: 'App',

  components: {
    NavBar,
    LandingSection,
    ProblemSection,
    RiskSection,
    SolutionSection,
    SellingPointSection,
    SkillsSection,
    ClassSection,
    StatisticSection,
    ContactUsSection
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
