<template>
  <div class="flex h-screen overflow-hidden">
    <NavigationBar />
    <main class="flex-1 overflow-y-auto">
      <HeroSection />
      <Projects />
    </main>
  </div>
</template>

<script lang="ts">
import HeroSection from './components/HeroSection.vue';
import NavigationBar from './components/NavigationBar.vue';
import Projects from './components/Projects.vue';


export default {
  components: { HeroSection, NavigationBar, Projects },
  data() {
    return {
    }
  },
}
</script>
