<script setup>
import { onMounted } from 'vue'
import AOS from 'aos'
import 'aos/dist/aos.css'
import Footer from '@/components/Footer.vue'

onMounted(() => {
  AOS.init({ once: true })
})
</script>

<template>
  <section class="max-w-4xl mx-auto p-6 bg-white rounded-lg font-[Poppins,sans-serif] mt-6 mb-12">
    <!-- Profile Header -->
    <div class="text-center border-b pb-6" data-aos="fade-down">
      <img
        src="@/assets/img/ako2.jpg"
        alt="Jun Gil Casquejo"
        class="w-32 h-32 mx-auto rounded-full shadow-lg mb-4 object-cover"
      />
      <h1 class="text-3xl font-bold text-gray-800">Jun Gil Casquejo</h1>
      <p class="text-lg text-gray-600">BSIT Student • Web Developer</p>
    </div>

    <!-- Contact Info -->
    <div class="mt-6" data-aos="fade-up">
      <h2 class="text-xl font-semibold text-gray-700 border-b mb-2">Contact</h2>
      <ul class="text-gray-600 space-y-1">
        <li><i class="fas fa-phone-alt text-green-500 mr-2"></i>+63 9568692103</li>
        <li><i class="fas fa-envelope text-blue-500 mr-2"></i>jungilcasquejo5@gmail.com</li>
        <li><i class="fas fa-map-marker-alt text-red-500 mr-2"></i>Calan 2, Poblacion, Cordova, Cebu</li>
        <li><i class="fas fa-birthday-cake text-pink-500 mr-2"></i>Birthday: June 03, 2003</li>
        <li><i class="fas fa-location-arrow text-purple-500 mr-2"></i>Place of Birth: Calan 2, Poblacion, Lapu-Lapu City, Cebu</li>
      </ul>
    </div>

    <!-- Education -->
    <div class="mt-6" data-aos="fade-up">
      <h2 class="text-xl font-semibold text-gray-700 border-b mb-2">Education</h2>
      <ul class="text-gray-600 list-disc list-inside">
        <li><span class="font-medium">Bachelor of Science in Information Technology (BSIT)</span> — 2021-2025</li>
        <li><span class="font-medium">Senior High Diploma</span>, Cordova National High School — 2016-2020</li>
        <li><span class="font-medium">High School Diploma</span>, Cordova National High School — 2012-2016</li>
      </ul>
    </div>

    <!-- About Me -->
    <div class="mt-6" data-aos="fade-up">
      <h2 class="text-xl font-semibold text-gray-700 border-b mb-2">About Me</h2>
      <p class="text-gray-600">
        BSIT student with a motivated attitude and a variety of powerful skills. Adept in various social media platforms and technology programs. Committed to contributing my expertise in a dynamic office or media production environment.
      </p>
    </div>

    <!-- Experience -->
    <div class="mt-6" data-aos="fade-up">
      <h2 class="text-xl font-semibold text-gray-700 border-b mb-2">Experience</h2>
      <ul class="text-gray-600 list-disc list-inside">
        <li><span class="font-medium">DepEd, Divisio of Lapu-lapu City</span> – Technical Support Representative (2023–2024)</li>
        <li><span class="font-medium">Solea Mactan Resort</span> – Service Crew (2024)</li>
        <li><span class="font-medium">Marigondon Food Park</span> – Service Crew (2023)</li>
      </ul>
    </div>
  </section>
  <Footer />
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');
</style>
