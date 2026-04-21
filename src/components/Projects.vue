<template>
  <div class="w-full flex flex-col min-h-screen p-1 bg-[#000c1d] items-center">
    <h1 class="text-6xl text-[#ffd60a] text-center pb-12 pt-12 font-bold!">
      My Projects
    </h1>
    <div class="flex flex-wrap justify-center gap-12 w-full max-w-7xl">
      <ProjectCard
        v-for="project in projectList"
        :key="project.title"
        :project="project"
      />
    </div>
  </div>
</template>

<script lang="ts">
import ProjectCard from './ProjectCard.vue';
import type { Projects } from '@/interfaces/Projects.ts';
import structrsImg from '@/images/Structrs.png';
import dailyAlbumImg from '@/images/Daily-Album.png';


export default {
  data () {
    return {
      projectList: [{
        title: 'Structrs',
        image: structrsImg,
        description: 'Organize your files easily with Structrs. Structrs is an agentic file organizer that determines where a newly downloaded file belongs and moves it in real time.'
      },
      {
        title: 'Daily Album',
        image: dailyAlbumImg,
        description: 'A mobile app that provides a daily album recommendation based off your Spotify statistics.'
      },
      {
        title: 'Journal To Do List',
        image: '../images/Journal.png',
        description: 'Manage your past present and future using Journal To Do List.'
      }] as Projects[]
    }
  },
  components: {
    ProjectCard
  }
};
</script>

<style>
.project {
  background-color: #001d3d;
  width: 500px;
  color: #d8f3dc;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  font-size: 20px;
  transition: transform 0.2s ease;
}

.project:hover {
  transform: scale(1.05);
}
</style>