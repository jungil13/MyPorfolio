<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'

const isOpen = ref(false)

const toggleMenu = () => {
  isOpen.value = !isOpen.value
}
</script>

<template>
  <header class="bg-white text-black font-[Poppins,sans-serif] shadow-md sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
      <!-- Logo -->
      <RouterLink to="/" class="hover:text-blue-400 text-blue-600 text-xl font-semi-bold transition-colors duration-300">
        JUN-GIL®
      </RouterLink>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex space-x-6 text-md">
        <RouterLink to="/about" class="hover:text-blue-400 transition duration-300">About</RouterLink>
        <RouterLink to="/projects" class="hover:text-blue-400 transition duration-300">Projects</RouterLink>
        <RouterLink to="/contact" class="hover:text-blue-400 transition duration-300">Resume</RouterLink>
      </nav>

      <!-- Hamburger Button (Mobile) -->
      <button class="md:hidden focus:outline-none" @click="toggleMenu">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
      </button>
    </div>

    <!-- Mobile Nav -->
    <div v-if="isOpen" class="md:hidden px-4 pb-4">
      <nav class="flex flex-col space-y-3 text-lg">
        <RouterLink to="/about" class="hover:text-blue-400 transition duration-300">About</RouterLink>
        <RouterLink to="/projects" class="hover:text-blue-400 transition duration-300">Projects</RouterLink>
        <RouterLink to="/contact" class="hover:text-blue-400 transition duration-300">Contact</RouterLink>
      </nav>
    </div>
  </header>
</template>
