<template>
  <section class="text-white mt-18" id="about">
    <!-- <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
      <div
        class="h-24 w-64 bg-gradient-to-br from-primary via-secondary blur-2xl to-[#570cac] opacity-20"
      ></div>
    </div> -->
    <div
      class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1"
    >
      <div data-aos="flip-right">
        <h2 class="text-4xl font-bold text-white mb-8 text-center">
          My Education
        </h2>
        <div class="space-y-8 py-8">
          <div
            v-for="element in education"
            :key="element.id"
            class="flex items-center md:w-[80%] w-full rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]"
          >
            <div class="w-1/4 p-5">
              <img
                src="https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png"
                alt="graduation-cap--v1"
              />
            </div>
            <div class="w-3/4 pl-4">
              <h3
                class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl"
              >
                {{ element.School }}
              </h3>
              <p class="text-white">{{ element.program }}</p>
              <p class="text-white">{{ element.year }}</p>
            </div>
          </div>
        </div>
      </div>
      <div
        class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full"
        data-aos="flip-right"
      >
        <h2
          class="text-4xl text-center font-bold text-white md:text-center mb-4"
        >
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary"
            >About</span
          >
          Me
        </h2>
        <p class="text-base text-center">
          Here's my info. I hope we can work together.
        </p>
        <div
          class="text-base lg:text-lg mt-8 py-8 grid grid-cols-2 gap-6 items-center"
        >
          <a
            href="mailto:tienlevan78py@gmail.com"
            class="flex gap-2 items-center"
            style="opacity: 1; transform: none"
            ><div
              class="p-3 text-[20px] shadow-xl rounded-[8px] h-full uppercase"
            >
              <svg
                stroke="currentColor"
                fill="currentColor"
                stroke-width="0"
                viewBox="0 0 1024 1024"
                height="1em"
                width="1em"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M928 160H96c-17.7 0-32 14.3-32 32v640c0 17.7 14.3 32 32 32h832c17.7 0 32-14.3 32-32V192c0-17.7-14.3-32-32-32zm-80.8 108.9L531.7 514.4c-7.8 6.1-18.7 6.1-26.5 0L189.6 268.9A7.2 7.2 0 0 1 194 256h648.8a7.2 7.2 0 0 1 4.4 12.9z"
                ></path>
              </svg>
            </div>
            <div class="">
              <h3
                class="font-semibold my-[-2px] text-orange-600 dark:text-white"
              >
                Email:
              </h3>
              <p class="text-gray-500 dark:text-white">
                tienlevan78py@gmail.com
              </p>
            </div></a
          >
          <a
            href="tel:(+84)338 203 413"
            class="flex gap-2 items-center"
            style="opacity: 1; transform: none"
            ><div
              class="p-3 text-[20px] shadow-xl rounded-[8px] h-full uppercase"
            >
              <svg
                stroke="currentColor"
                fill="currentColor"
                stroke-width="0"
                viewBox="0 0 1024 1024"
                height="1em"
                width="1em"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M744 62H280c-35.3 0-64 28.7-64 64v768c0 35.3 28.7 64 64 64h464c35.3 0 64-28.7 64-64V126c0-35.3-28.7-64-64-64zM512 824c-22.1 0-40-17.9-40-40s17.9-40 40-40 40 17.9 40 40-17.9 40-40 40z"
                ></path>
              </svg>
            </div>
            <div class="">
              <h3
                class="font-semibold my-[-2px] text-orange-600 dark:text-white"
              >
                Phone Number:
              </h3>
              <p class="text-gray-500 dark:text-white">0338203413</p>
            </div></a
          >
          <a
            href="https://github.com/TienVannnn"
            class="flex gap-2 items-center"
            style="opacity: 1; transform: none"
            ><div
              class="p-3 text-[20px] shadow-xl rounded-[8px] h-full uppercase"
            >
              <svg
                stroke="currentColor"
                fill="currentColor"
                stroke-width="0"
                viewBox="0 0 1024 1024"
                height="1em"
                width="1em"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M511.6 76.3C264.3 76.2 64 276.4 64 523.5 64 718.9 189.3 885 363.8 946c23.5 5.9 19.9-10.8 19.9-22.2v-77.5c-135.7 15.9-141.2-73.9-150.3-88.9C215 726 171.5 718 184.5 703c30.9-15.9 62.4 4 98.9 57.9 26.4 39.1 77.9 32.5 104 26 5.7-23.5 17.9-44.5 34.7-60.8-140.6-25.2-199.2-111-199.2-213 0-49.5 16.3-95 48.3-131.7-20.4-60.5 1.9-112.3 4.9-120 58.1-5.2 118.5 41.6 123.2 45.3 33-8.9 70.7-13.6 112.9-13.6 42.4 0 80.2 4.9 113.5 13.9 11.3-8.6 67.3-48.8 121.3-43.9 2.9 7.7 24.7 58.3 5.5 118 32.4 36.8 48.9 82.7 48.9 132.3 0 102.2-59 188.1-200 212.9a127.5 127.5 0 0 1 38.1 91v112.5c.8 9 0 17.9 15 17.9 177.1-59.7 304.6-227 304.6-424.1 0-247.2-200.4-447.3-447.5-447.3z"
                ></path>
              </svg>
            </div>
            <div class="">
              <h3
                class="font-semibold my-[-2px] text-orange-600 dark:text-white"
              >
                Github:
              </h3>
              <p class="text-gray-500 dark:text-white">TienVannnn</p>
            </div></a
          >
          <a
            href="https://www.facebook.com/profile.php?id=100029818574884"
            class="flex gap-2 items-center"
            style="opacity: 1; transform: none"
            ><div
              class="p-3 text-[20px] shadow-xl rounded-[8px] h-full uppercase"
            >
              <svg
                stroke="currentColor"
                fill="currentColor"
                stroke-width="0"
                viewBox="0 0 1024 1024"
                height="1em"
                width="1em"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M880 112H144c-17.7 0-32 14.3-32 32v736c0 17.7 14.3 32 32 32h736c17.7 0 32-14.3 32-32V144c0-17.7-14.3-32-32-32zm-92.4 233.5h-63.9c-50.1 0-59.8 23.8-59.8 58.8v77.1h119.6l-15.6 120.7h-104V912H539.2V602.2H434.9V481.4h104.3v-89c0-103.3 63.1-159.6 155.3-159.6 44.2 0 82.1 3.3 93.2 4.8v107.9z"
                ></path>
              </svg>
            </div>
            <div class="">
              <h3
                class="font-semibold my-[-2px] text-orange-600 dark:text-white"
              >
                Facebook:
              </h3>
              <p class="text-gray-500 dark:text-white">Văn Tiến</p>
            </div></a
          >
        </div>
        <!-- <div class="grid grid-cols-3 gap-4 max-w-lg pt-8">
          <div
            class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3"
          >
            <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">
              +200
            </h3>
            <p class="text-sm sm:text-base text-gray-300">Happy Client</p>
          </div>
          <div
            class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3"
          >
            <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">
              +300
            </h3>
            <p class="text-sm sm:text-base text-gray-300">Project</p>
          </div>

          <div
            class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3"
          >
            <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">
              +7
            </h3>
            <p class="text-sm sm:text-base text-gray-300">Years Experience</p>
          </div>
        </div> -->
      </div>
    </div>
  </section>
</template>
<script setup>
import { ref } from 'vue'
const education = ref([
  {
    id: 1,
    School: 'Nha Trang University',
    program: 'Software Engineer',
    year: '2021',
  },
])
</script>
