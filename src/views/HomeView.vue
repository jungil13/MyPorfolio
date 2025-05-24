<script setup>
import { onMounted } from 'vue'
import AOS from 'aos'
import 'aos/dist/aos.css'
import { Github, Facebook, Instagram } from 'lucide-vue-next'
import Projects from '@/views/Projects.vue'
import Footer from '@/components/Footer.vue'

onMounted(() => {
  AOS.init({ once: true })
})
</script>

<template>
  <!-- INTRO SECTION -->
  <section class="top-0 min-h-screen flex items-center justify-center text-black px-4 md:px-16 font-[Poppins,sans-serif] bg-white">
    <div class="grid md:grid-cols-2 gap-12 items-center max-w-7xl w-full py-16" data-aos="fade-up">
      <!-- Left: Text & Socials -->
      <div class="space-y-6">
        <h1 class="text-4xl md:text-5xl font-bold leading-tight text-blue-600">Hi, I'm Jun Gil Casquejo</h1>
        <p class="text-lg md:text-xl text-gray-700">
          A passionate Web Developer who builds modern and responsive websites using Vue and Tailwind CSS.
        </p>

        <!-- Socials -->
        <div class="flex gap-6 pt-4">
          <a href="https://github.com/jungil13" target="_blank" class="text-gray-600 hover:text-black transition">
            <Github class="w-6 h-6" />
          </a>
          <a href="https://web.facebook.com/jungil.casquejo30" target="_blank" class="text-blue-600 hover:text-blue-800 transition">
            <Facebook class="w-6 h-6" />
          </a>
          <a href="https://www.instagram.com/jungilcasquejo_" target="_blank" class="text-pink-500 hover:text-pink-700 transition">
            <Instagram class="w-6 h-6" />
          </a>
        </div>
      </div>

      <!-- Right: Animated Image -->
      <div class="relative w-fit mx-auto" data-aos="zoom-in">
        <div class="absolute inset-0  rounded-full blur-xl opacity-40 scale-110"></div>
        <img src="@/assets/img/ako1.jpg" alt="Jun Gil" class="rounded-full shadow-md shadow-black w-80 h-80 md:w-100 md:h-100 object-cover relative z-10" />
      </div>
    </div>
  </section>

  <!-- PROJECTS SECTION -->
  <section class="bg-white text-gray-900 py-20 px-4 md:px-16 font-[Poppins,sans-serif] ">
    <div class="max-w-7xl mx-auto px-4 mt-12 mb-18">
        <h2 class="text-3xl md:text-4xl font-bold mb-12 text-center" data-aos="fade-up">
            My Projects
        </h2>

        <div class="grid gap-10 sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-4" data-aos="fade-up">
            <!-- Project 1 -->
            <RouterLink :to="{ name: 'ProjectDetails', params: { id: 'cordova-pet-hub' } }">

                <div
                    class="bg-white rounded-xl shadow-sm shadow-black overflow-hidden transform hover:-translate-y-2 hover:shadow-xl transition-all duration-300 cursor-pointer">
                    <div class="overflow-hidden">
                        <img src="@/assets/img/pet.png" alt="Project 1"
                            class="w-full h-48 object-cover transition-transform duration-500 hover:scale-105" />
                    </div>
                    <div class="p-5">
                        <h3 class="text-xl font-semibold mb-2">CORDOVA PET HUB</h3>
                        <p class="text-gray-600 text-sm lowercase">A PET ADOPTION SYSTEM FOR CORDOVA LOCALS AND A
                            CAPSTONE PROJECT.</p>
                    </div>
                </div>
            </RouterLink>
            <!-- Project 2 -->
            <RouterLink :to="{ name: 'ProjectDetails', params: { id: 'suroy-ta' } }">
                <div
                    class="bg-white rounded-xl shadow-sm shadow-black overflow-hidden transform hover:-translate-y-2 hover:shadow-xl transition-all duration-300 cursor-pointer">
                    <div class="overflow-hidden">
                        <img src="@/assets/img/suroy.png" alt="Project 2"
                            class="w-full h-48 object-cover transition-transform duration-500 hover:scale-105" />
                    </div>
                    <div class="p-5 ">
                        <h3 class="text-xl font-semibold mb-2">SUROY - TA</h3>
                        <p class="text-gray-600 text-sm lowercase">A BLOGGING WEBSITE FOR FAMOUS TOURISTS SPOT OF CEBU
                            CITY, PHILIPPINES .</p>
                    </div>
                </div>
            </RouterLink>
            <!-- Project 3 -->
            <RouterLink :to="{ name: 'ProjectDetails', params: { id: 'island-hoper' } }">
                <div
                    class="bg-white rounded-xl shadow-sm shadow-black overflow-hidden transform hover:-translate-y-2 hover:shadow-xl transition-all duration-300 cursor-pointer">
                    <div class="overflow-hidden">
                        <img src="@/assets/img/island.jfif" alt="Project 3"
                            class="w-full h-48 object-cover transition-transform duration-500 hover:scale-105" />
                    </div>
                    <div class="p-5">
                        <h3 class="text-xl font-semibold mb-2">ISLAND - HOPER</h3>
                        <p class="text-gray-600 text-sm">A booking system for island hoping at Cebu City, Cordova,
                            Philippines.</p>
                    </div>
                </div>
            </RouterLink>
            <!-- Project 4 -->
            <RouterLink :to="{ name: 'ProjectDetails', params: { id: 'spotichat' } }">

                <div
                    class="bg-white rounded-xl shadow-sm shadow-black overflow-hidden transform hover:-translate-y-2 hover:shadow-xl transition-all duration-300 cursor-pointer">
                    <div class="overflow-hidden">
                        <img src="@/assets/img/spotichat.png" alt="Project 4"
                            class="w-full h-48 object-cover transition-transform duration-500 hover:scale-105" />
                    </div>
                    <div class="p-5">
                        <h3 class="text-xl font-semibold mb-2">SPOTICHAT</h3>
                        <p class="text-gray-600 text-sm">Spotify is a project that has messaging feautures and uses Spotify Api.</p>
                    </div>
                </div>
            </RouterLink>
        </div>
    </div>
    <!-- More Projects Button -->
    <div class="mt-12 text-center">
  <RouterLink
    to="/projects"
    class="inline-block bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700 transition duration-300"
    data-aos="fade-up"
  >
    View More Projects
  </RouterLink>
</div>

  </section>
  <Footer />

</template>
