<template>
  <section class="text-white mt-20" id="projects">
    <div class="px-4 xl:px-16">
      <div class="mb-8 md:flex md:justify-between">
        <h2 class="text-4xl font-bold text-white">A Few Projects</h2>
      </div>
      <ul
        class="grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 lg:grid-cols-3"
        data-aos="fade-right"
      >
        <li v-for="project in Projects" :key="project.id">
          <div
            class="relative group overflow-hidden rounded-xl shadow-lg transition-transform duration-300 transform hover:scale-105"
          >
            <div
              class="h-64 bg-cover bg-center"
              :style="{ backgroundImage: 'url(' + project.image + ')' }"
            ></div>

            <div
              class="absolute inset-0 flex flex-col items-center justify-center bg-black bg-opacity-0 opacity-0 transition-all duration-500 group-hover:bg-opacity-50 group-hover:opacity-100"
            >
              <div class="text-center text-white p-4">
                <p class="text-gray-300 mt-2">{{ project.description }}</p>
                <div class="flex flex-wrap justify-center gap-2 mt-4">
                  <span
                    v-for="technology in project.technologies"
                    :key="technology"
                    class="px-2 py-1 bg-gray-800 rounded-full text-sm text-gray-300"
                  >
                    {{ technology }}
                  </span>
                </div>
                <div class="flex space-x-4 mt-4 justify-center">
                  <a
                    title="View Live"
                    :href="project.webURL"
                    class="w-10 h-10 flex items-center justify-center border border-gray-400 rounded-full hover:border-white transition duration-300"
                    aria-label="Website Link"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                      class="w-6 h-6 text-gray-300 hover:text-white"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M17.25 6.75L22.5 12l-5.25 5.25m-10.5 0L1.5 12l5.25-5.25m7.5-3-4.5 16.5"
                      />
                    </svg>
                  </a>
                  <a
                    title="View Source"
                    :href="project.gitURL"
                    class="w-10 h-10 flex items-center justify-center border border-gray-400 rounded-full hover:border-white transition duration-300"
                    aria-label="GitHub Link"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                      class="w-6 h-6 text-gray-300 hover:text-white"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M2.036 12.322a1.012 1.012 0 010-.639C3.423 7.51 7.36 4.5 12 4.5c4.638 0 8.573 3.007 9.963 7.178.07.207.07.431 0 .639C20.577 16.49 16.64 19.5 12 19.5c-4.638 0-8.573-3.007-9.963-7.178Z"
                      />
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M15 12a3 3 0 11-6 0 3 3 0 016 0Z"
                      />
                    </svg>
                  </a>
                </div>
              </div>
            </div>
          </div>
          <div
            class="text-white text-center rounded-b-xl mt-3 bg-[#111a3e] shadow-lg border border-[#1f1641] py-6 px-4"
          >
            <h3 class="text-lg font-semibold uppercase lg:text-xl">
              {{ project.title }}
            </h3>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
const Projects = ref([
  {
    id: 1,
    image: 'src/assets/images/projects/weatherapp.png',
    title: 'Weather web app',
    description:
      'Description: The website allows users to search for the city they want to see the weather and save that city for later viewing',
    technologies: ['vue.js 3', 'vuex'],
    gitURL: 'https://github.com/TienVannnn/Weather-App-Vuejs',
    webURL: 'weather-app-alpha-nine-23.vercel.app',
  },
  {
    id: 2,
    image: 'src/assets/images/projects/flipcard.png',
    title: 'Pokemon-FlipCard',
    description: 'website allows players to choose game modes',
    technologies: ['vue.js 3', 'vuex'],
    gitURL: 'https://github.com/TienVannnn/FlipCart-PokemonMemories',
    webURL: 'https://thunderous-heliotrope-f452ad.netlify.app/',
  },
  {
    id: 3,
    image: 'src/assets/images/projects/project.png',
    title: 'project 1',
    description:
      'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic tenetur quasi ipsam labore sapiente, accusamus necessitatibus laboriosam non voluptas inventore deserunt dolore modi ex, praesentium at provident nihil magni ratione!',
    technologies: ['vue.js 3', 'vuex', 'Express'],
    gitURL: '',
    webURL: '',
  },
  {
    id: 4,
    image: 'src/assets/images/projects/mobile.jpg',
    title: 'project 1',
    description:
      'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic tenetur quasi ipsam labore sapiente, accusamus necessitatibus laboriosam non voluptas inventore deserunt dolore modi ex, praesentium at provident nihil magni ratione!',
    technologies: ['vue.js 3', 'vuex', 'Express'],
    gitURL: '',
    webURL: '',
  },
])
</script>
