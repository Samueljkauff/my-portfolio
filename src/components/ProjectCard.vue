<template>
  <div class="project">
    <img :src="project.image" class="w-full h-70 object-cover rounded-md" />
    <h2 class="text-2xl font-bold! text-[#ffd60a] pt-4">{{ project.title }}</h2>
    <p class="text-sm text-[#d8f3dc]/70 mt-2">{{ project.description }}</p>
  </div>
</template>

<script lang="ts">
import type { Projects } from '@/interfaces/projects';

export default {
  props: {
    project: {
      type: Object as () => Projects,
      required: true,
    }
  }
}
</script>