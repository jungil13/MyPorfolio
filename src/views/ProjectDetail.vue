<template>
  <div class="max-w-4xl mx-auto p-6 mt-10 space-y-6" data-aos="fade-up">
    <h1
      class="text-4xl font-extrabold mb-4 text-center text-gray-800 hover:text-blue-600 transition-colors duration-300"
      data-aos="fade-down"
    >
      {{ project?.title }}
    </h1>

    <div class="overflow-hidden rounded-xl shadow-lg" data-aos="zoom-in">
      <img
        v-if="project"
        :src="project.image"
        alt="Project"
        class="w-full h-[350px] object-cover transition-transform duration-500 hover:scale-105"
      />
    </div>

    <div class="bg-white p-6 rounded-xl shadow-md" data-aos="fade-up">
      <p class="text-gray-700 text-lg leading-relaxed">
        {{ project?.description }}
      </p>

      <!-- Additional info -->
      <p class="text-gray-600 mt-4 text-md">
        This project showcases a complete web-based solution tailored to its purpose. It leverages modern web development tools including <strong>Vue.js</strong>, <strong>Tailwind CSS</strong>, and backend integration. The UI is designed to be clean, responsive, and user-friendly. It also highlights your ability to deliver real-world solutions and full-stack capabilities.
      </p>
    </div>

    <RouterLink
      to="/projects"
      class="text-blue-600 hover:text-blue-800 hover:underline transition mt-6 inline-block text-lg font-medium"
    >
      ← Back to Projects
    </RouterLink>
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router'
import { computed, onMounted } from 'vue'
import AOS from 'aos'
import 'aos/dist/aos.css'

// Initialize AOS
onMounted(() => {
  AOS.init({
    duration: 800,
    once: true,
  })
})

const images = import.meta.glob('@/assets/img/*', { eager: true, as: 'url' })

const projects = [
  {
    id: 'cordova-pet-hub',
    title: 'CORDOVA PET HUB',
    image: images['/src/assets/img/defend.jpg'],
    description:
      'CORDOVA PET HUB is a web-based pet adoption platform dedicated to the locals of Cordova. It serves as a centralized system for reporting lost and found pets, adopting rescued animals, and connecting pet lovers with each other. As a capstone project, it demonstrates database integration, user authentication, and intuitive UX design.'
  },
  {
    id: 'suroy-ta',
    title: 'SUROY - TA',
    image: images['/src/assets/img/suroy.png'],
    description:
      'SUROY - TA is a blogging website showcasing the most famous tourist spots of Cebu City. It allows users to share experiences, rate destinations, and explore hidden gems. The platform is built with a focus on community engagement and tourism promotion.'
  },
  {
    id: 'island-hoper',
    title: 'ISLAND - HOPER',
    image: images['/src/assets/img/island.jfif'],
    description:
      'ISLAND - HOPER is a booking system for island-hopping tours around Cebu City and Cordova. The system supports schedule management, trip reservations, and user reviews, streamlining the booking experience for tourists and operators.'
  },
  {
    id: 'spotichat',
    title: 'SPOTICHAT',
    image: images['/src/assets/img/spotichat.png'],
    description:
      'SPOTICHAT is a Spotify-inspired web application that integrates messaging features. It combines music streaming with real-time chat functionality, offering users a unique social listening experience.'
  }
]

const route = useRoute()
const projectId = route.params.id
const project = computed(() => projects.find(p => p.id === projectId))
</script>
