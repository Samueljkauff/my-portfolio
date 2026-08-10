<template>
  <div
    class="flex min-h-screen w-full flex-col items-center justify-center gap-10 px-6 py-12
           md:flex-row md:justify-around md:gap-12 md:px-12
           lg:px-20"
  >
    <div class="flex w-full max-w-2xl flex-col">
      <p class="text-secondary text-lg tracking-widest uppercase sm:text-xl">
        Hello,
      </p>

      <h1
        class="text-4xl font-bold text-[#cad2c5]
               sm:text-5xl
               md:text-6xl
               lg:text-7xl"
      >
        I'm
        <span class="text-secondary font-bold!">
          Sam Kauffman
        </span>
      </h1>

      <div
        class="mt-4 w-full text-base leading-relaxed text-secondary/80
               sm:text-lg
               md:text-xl"
      >
        I am a full stack web developer located in Louisville Kentucky. I graduated from
        <a
          href="https://www.bellarmine.edu/"
          class="text-secondary transition-colors duration-200 hover:text-[#cad2c5]"
        >
          Bellarmine University
        </a>
        in May 2026 with a bachelor of arts in computer science. I focus on building stylish and
        responsive websites with user experience in mind.
      </div>

      <div class="flex h-auto gap-6 py-5">
        <a
          href="https://www.linkedin.com/in/sam-kauffman-0354b6271/"
          target="_blank"
          rel="noopener noreferrer"
        >
          <i class="pi pi-linkedin social-icon"></i>
        </a>

        <a
          href="https://github.com/Samueljkauff"
          target="_blank"
          rel="noopener noreferrer"
        >
          <i class="pi pi-github social-icon"></i>
        </a>

        <a
          href="https://www.instagram.com/s4mu31k/?hl=en"
          target="_blank"
          rel="noopener noreferrer"
        >
          <i class="pi pi-instagram social-icon"></i>
        </a>
      </div>

      <a
        href="mailto:samueljkauff@gmail.com"
        class="w-full sm:w-fit"
      >
        <button
          class="h-12 w-full cursor-pointer rounded-md border border-secondary px-6
                 text-secondary transition-colors duration-200
                 hover:bg-[#ffd60a] hover:text-[#000814]
                 sm:w-auto"
        >
          Contact Me
        </button>
      </a>
    </div>

    <div
      class="hidden shrink-0 overflow-hidden rounded-full
             ring-4 ring-[#ffd60a] shadow-2xl
             md:block md:h-72 md:w-72
             lg:h-96 lg:w-96
             xl:h-[30rem] xl:w-[30rem]"
    >
      <img
        class="h-full w-full object-cover"
        src="../images/headshot.JPG"
        alt="Sam Kauffman"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import 'primeicons/primeicons.css';
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