<template>
  <div id="app">
    <AppHeader />
    <main>
      <HeroSection />
      <FeaturesSection />
      <ScreenshotsSection />
      <DownloadSection />
      <TechSection />
    </main>
    <AppFooter />
  </div>
</template>

<script setup>
import AppHeader from './components/AppHeader.vue'
import HeroSection from './components/HeroSection.vue'
import FeaturesSection from './components/FeaturesSection.vue'
import ScreenshotsSection from './components/ScreenshotsSection.vue'
import DownloadSection from './components/DownloadSection.vue'
import TechSection from './components/TechSection.vue'
import AppFooter from './components/AppFooter.vue'
</script>

<style scoped>
#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

main {
  flex: 1;
}
</style>
