<template>
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
          <a href="https://github.com/jungil13" target="_blank" class="hover:text-blue-400 text-xl">
            <i class="fab fa-github"></i>
          </a>
          <a href="https://web.facebook.com/jungil.casquejo30" target="_blank" class="hover:text-blue-400 text-xl">
            <i class="fab fa-facebook"></i>
          </a>
          <a href="https://www.instagram.com/jungilcasquejo_" target="_blank" class="hover:text-blue-400 text-xl">
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
