<script setup>
import { onMounted } from 'vue'
import AOS from 'aos'
import 'aos/dist/aos.css'

onMounted(() => {
  AOS.init({ once: true })
})
</script>

<template>
  <section class="min-h-screen bg-white text-black px-4 py-20 font-[Poppins,sans-serif]">
    <div class="max-w-7xl mx-auto grid gap-10 md:grid-cols-2 items-center" data-aos="fade-up">
      
      <!-- Text Section -->
      <div>
        <h2 class="text-4xl md:text-5xl font-bold mb-6">About Me</h2>
        <p class="text-lg text-gray-700 mb-4">
          Hello! I'm <strong>Jun Gil Casquejo</strong>, a passionate web developer focused on building fast, responsive, and accessible websites using technologies like <span class="text-blue-600 font-semibold">Vue.js</span> and <span class="text-blue-600 font-semibold">Tailwind CSS</span>.
        </p>
        <p class="text-lg text-gray-700 mb-4">
          I enjoy turning ideas into reality through clean and user-friendly designs. With a keen eye for detail and a love for learning, I'm constantly improving and exploring new tools and frameworks.
        </p>
        <p class="text-lg text-gray-700">
          When I'm not coding, I enjoy exploring new places, watching tech videos, and working on creative side projects.
        </p>
      </div>

      <!-- Image Section -->
      <div class="flex justify-center md:justify-end">
        <img
          src="@/assets/img/ako.jpg"
          alt="Jun Gil"
          class="w-70 h-90 md:w-80 md:h-100 object-cover rounded-full shadow-xl border-4 "
          data-aos="zoom-in"
        />
      </div>
      <p class="text-lg text-blue-700 text-center md:text-start">
         @ Jun Gil Casquejo
        </p>
    </div>
  </section>
  <footer class="bg-gray-900 text-white py-10 font-[Poppins,sans-serif]">
    <div class="max-w-7xl mx-auto px-4 grid gap-6 md:grid-cols-2 lg:grid-cols-3 text-center md:text-left">
      
      <!-- Logo + Intro -->
      <div>
        <h2 class="text-2xl font-bold mb-2">J U N - G I L</h2>
        <p class="text-gray-400 text-sm">Web Developer passionate about building beautiful and responsive websites.</p>
      </div>

      <!-- Quick Links -->
      <div>
        <h3 class="text-xl font-semibold mb-2">Quick Links</h3>
        <ul class="space-y-2 text-sm text-gray-300">
          <li><RouterLink to="/" class="hover:text-blue-400 transition">Home</RouterLink></li>
          <li><RouterLink to="/about" class="hover:text-blue-400 transition">About</RouterLink></li>
          <li><RouterLink to="/projects" class="hover:text-blue-400 transition">Projects</RouterLink></li>
          <li><RouterLink to="/contact" class="hover:text-blue-400 transition">Resume</RouterLink></li>
        </ul>
      </div>

      <!-- Social Media -->
      <div>
        <h3 class="text-xl font-semibold mb-2">Follow Me</h3>
        <div class="flex justify-center md:justify-start space-x-4">
          <a href="https://github.com/yourusername" target="_blank" class="hover:text-blue-400 text-xl">
            <i class="fab fa-github"></i>
          </a>
          <a href="https://facebook.com/yourusername" target="_blank" class="hover:text-blue-400 text-xl">
            <i class="fab fa-facebook"></i>
          </a>
          <a href="https://instagram.com/yourusername" target="_blank" class="hover:text-blue-400 text-xl">
            <i class="fab fa-instagram"></i>
          </a>
        </div>
      </div>
    </div>

    <!-- Bottom -->
    <div class="text-center text-sm text-gray-500 mt-8">
      © {{ new Date().getFullYear() }} Jun Gil Casquejo. All rights reserved.
    </div>
  </footer>
</template>
