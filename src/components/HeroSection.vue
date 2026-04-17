<template>
  <NavigationBar/>
  <div class="flex flex-col-2 items-center gap-12">
    <div class="items-center">
      <h1 class="text-5xl font-bold">Hello, I'm Sam Kauffman</h1>
      <h2 class="text-xl mt-2">Computer Science | Full Stack</h2>
      <p class="text-lg mt-2">
        <a href="https://www.bellarmine.edu/">Bellarmine University</a> 2026 Graduate
      </p>
    </div>
    <div class="flex justify-center items-center">
      <img class="max-w-sm w-full h-auto" src="../images/headshot.png" />
    </div>
  </div>
</template>

<script lang="ts">
import NavigationBar from './NavigationBar.vue';


export default {
  data() {
    return {

    }
  },
  components: {
    NavigationBar
  }
}
</script>
