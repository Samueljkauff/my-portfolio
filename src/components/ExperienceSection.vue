<template>
  <div class="h-screen flex justify-center items-center">
    <div class="flex flex-col gap-5 h-3/4 w-3/4 bg-[#001d3d] rounded-lg p-10">
      <h1 class="text-6xl font-bold! text-[#ffd60a] text-center">My Experience</h1>
      <hr class="border-[#ffd60a33]">

      <div class="flex gap-6">
        <div v-for="job in experience" :key="job.title" class="flex flex-col gap-3 flex-1 bg-[#000814] rounded-lg p-5 border border-[#ffd60a18] hover:border-[#ffd60a44] transition-colors duration-200">
          <img :src="job.image" :alt="job.title" class="w-16 h-16 rounded-full object-cover border-2 border-[#ffd60a44]" />
          <div>
            <h2 class="text-[#ffd60a] font-semibold text-lg">{{ job.title }}</h2>
            <p class="text-[#cad2c5] text-sm opacity-60">{{ job.position }}</p>
          </div>
          <p class="text-[#cad2c5] text-md opacity-80 leading-relaxed">{{ job.description }}</p>
        </div>
      </div>

    </div>
  </div>
</template>

<script lang="ts">
import concord from '@/images/Concord.jpeg';
import vividus from '@/images/Vividus-labs.png'

export default {
  data() {
    return {
      experience: [
        {
          image: concord,
          title: 'Concord Energy Strategies',
          position: 'Web Dev Intern',
          description: 'Worked in a small agile team to design and build a SaaS web application. Contributed to both frontend and backend development using Vue, TypeScript, Tailwind, Laravel, Inertia, and Vite. Managed tasks through Jira and collaborated via GitHub with a pull request review process requiring two approvals before merging.',
        },
        {
          image: vividus,
          title: 'Vividus Labs',
          position: 'QA Tester',
          description: 'Worked in a small team testing SaaS web applications to find and report bugs before they shipped. Managed and tracked tickets through Monday.com to keep everything organized across the team.',
        },
      ],
    }
  },
}
</script>
