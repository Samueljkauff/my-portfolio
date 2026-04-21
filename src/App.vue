<template>
  <div class="flex h-screen overflow-hidden">
    <NavigationBar />
    <main class="flex-1 overflow-y-auto">
      <HeroSection id="about" />
      <Projects id="projects" />
      <ExperienceSection id="experience" />
      <!-- <CommentSection id="comments" /> -->
    </main>
  </div>
</template>

<script lang="ts">
import CommentSection from './components/CommentSection.vue';
import ExperienceSection from './components/ExperienceSection.vue';
import HeroSection from './components/HeroSection.vue';
import NavigationBar from './components/NavigationBar.vue';
import Projects from './components/Projects.vue';


export default {
  components: { HeroSection, NavigationBar, Projects, CommentSection, ExperienceSection },
  data() {
    return {
    }
  },
}
</script>
