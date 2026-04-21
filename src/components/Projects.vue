<template>
  <div class="w-full flex flex-col min-h-screen p-1 bg-[#000c1d] items-center">
    <h1 v-if="section == 'code'" class="text-6xl text-[#ffd60a] text-center pb-12 pt-12 font-bold!">
      My Code Projects
    </h1>
    <h1 v-if="section == 'design'" class="text-6xl text-[#ffd60a] text-center pb-12 pt-12 font-bold!">
      My Design Projects
    </h1>
    <div class="flex flex-wrap justify-center gap-12 w-full max-w-7xl">
    <a
      v-for="project in projectList.filter(p => p.type === section)"
      :key="project.title"
      :href="project.link"
      target="_blank"
      rel="noopener noreferrer">
      <ProjectCard :project="project"
      />
    </a>
    </div>
  </div>
</template>

<script lang="ts">
import ProjectCard from './ProjectCard.vue';
import structrsImg from '@/images/Structrs.png';
import dailyAlbumImg from '@/images/Daily-Album.png';
import journalImg from '@/images/Journal.png';
import jwtFlowImg from '@/images/JwtFlow.png';
import type { Projects } from '@/interfaces/projects';


export default {
  data () {
    return {
      projectList: [{
        title: 'Structrs',
        image: structrsImg,
        description: 'Organize your files easily with Structrs. Structrs is an agentic file organizer that determines where a newly downloaded file belongs and moves it in real time.',
        link: 'https://github.com/Samueljkauff/Structrs',
        type: 'code'
      },
      {
        title: 'Daily Album',
        image: dailyAlbumImg,
        description: 'A mobile app that provides a daily album recommendation based off your Spotify statistics.',
        link: 'https://github.com/Samueljkauff/daily-album',
        type: 'code'
      },
      {
        title: 'Journal To Do List',
        image: journalImg,
        description: 'Manage your past present and future using Journal To Do List.',
        link: 'https://github.com/Samueljkauff/Journal-and-To-Do-List',
        type: 'code'
      },
      {
        title: 'JWT Auth Flow',
        image: jwtFlowImg,
        description: 'An infograph designed and created by me using infogram.com. This infogram explains a classic, simplified JWT flow.',
        link: 'https://infogram.com/jwt-login-poster-1h9j6q75ked5v4g',
        type: 'design',
      },
      {
        title: '',
        image: 'place',
        description: '',
        link: '',
        type: 'design',
      }] as Projects[]
    }
  },
  props: {
    section: {
      type: String,
      default: "Projects",
      required: true,
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
