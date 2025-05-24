<template>
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
    <footer class="bg-gray-900 text-white py-10 font-[Poppins,sans-serif]">
        <div class="max-w-7xl mx-auto px-4 grid gap-6 md:grid-cols-2 lg:grid-cols-3 text-center md:text-left">

            <!-- Logo + Intro -->
            <div>
                <h2 class="text-2xl font-bold mb-2">J U N - G I L</h2>
                <p class="text-gray-400 text-sm">Web Developer passionate about building beautiful and responsive
                    websites.</p>
            </div>

            <!-- Quick Links -->
            <div>
                <h3 class="text-xl font-semibold mb-2">Quick Links</h3>
                <ul class="space-y-2 text-sm text-gray-300">
                    <li>
                        <RouterLink to="/" class="hover:text-blue-400 transition">Home</RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/about" class="hover:text-blue-400 transition">About</RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/projects" class="hover:text-blue-400 transition">Projects</RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/contact" class="hover:text-blue-400 transition">Resume</RouterLink>
                    </li>
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
