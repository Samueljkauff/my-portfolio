<template>
  <div class="flex items-center justify-around h-screen px-20">
    <div class="flex flex-col">
      <p class="text-[#ffc300] text-lg tracking-widest uppercase">Hello,</p>
      <h1 class="text-6xl font-bold text-[#cad2c5]">
        I'm <span class="text-[#ffd60a]">Sam Kauffman</span>
      </h1>
      <p class="text-lg text-[#ffc300]/80">
        I am a full stack web developer located in Louisville Kenucky. <br> I graduated from
        <a
          href="https://www.bellarmine.edu/"
          class="text-[#ffd60a] hover:text-[#cad2c5] transition-colors duration-200"
          >Bellarmine University</a
        >
        in 2026 with a bachalor <br> of arts in computer science.
      </p>
      <div class="flex gap-6 pt-4">
        <a href="https://www.linkedin.com/in/sam-kauffman-0354b6271/" target="_blank">
          <i class="pi pi-linkedin social-icon"></i>
        </a>
        <a href="https://github.com/Samueljkauff">
          <i class="pi pi-github social-icon"></i>
        </a>
        <a href="https://www.instagram.com/s4mu31k/?hl=en">
          <i class="pi pi-instagram social-icon"></i>
        </a>
      </div>
    </div>
    <div class="rounded-full overflow-hidden w-80 h-80 ring-4 ring-[#ffd60a] shadow-2xl">
      <img class="w-full h-full object-cover" src="../images/headshot.JPG" />
    </div>
  </div>
</template>

<script lang="ts">
import 'primeicons/primeicons.css'

export default {
  data() {
    return {}
  },
}
</script>

<style>
.social-icon {
  font-size: 22px;
  color: #ffc300;
  opacity: 0.6;
  cursor: pointer;
  transition:
    opacity 0.2s ease,
    transform 0.2s ease;
}

.social-icon:hover {
  opacity: 1;
  transform: translateY(-3px);
}
</style>
