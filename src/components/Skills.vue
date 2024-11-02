<template>
  <section class="text-white mt-20" id="skills">
    <div class="px-4 xl:pl-16">
      <h2
        class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary mb-4 text-center"
      >
        My Skills
      </h2>
      <p class="text-white text-center">
        Here are some of the skill I've. I hope it will meet your requirements.
      </p>
    </div>
    <div
      class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-2 gap-6 pt-10 sm:grid-cols-3 md:gap-10 md:pt-12 lg:grid-cols-4 2xl:grid-cols-5"
    >
      <a
        v-for="service in services"
        :href="service.href"
        :key="service.id"
        data-aos="fade-up"
        target="_blank"
        class="px-8 py-12 rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] hover-effect"
      >
        <div class="mx-auto h-24 w-24 text-center xl:h-28 xl:w-28">
          <div>
            <img :src="service.icon" alt="service icon" />
          </div>
        </div>
        <div class="text-center">
          <h3
            class="pt-8 text-lg font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl"
          >
            {{ service.name }}
          </h3>
          <p class="text-grey pt-4 text-sm group-hover:text-white md:text-base">
            {{ service.description }}
          </p>
        </div>
      </a>
    </div>
  </section>
</template>
<script setup>
import { ref } from 'vue'
import htmlIcon from '../assets/images/html.png'
import cssIcon from '../assets/images/css.png'
import jsIcon from '../assets/images/js.png'
import phpIcon from '../assets/images/php.png'
import aspIcon from '../assets/images/asp.png'
import btIcon from '../assets/images/bootstrap.png'
import tlIcon from '../assets/images/tailwind.png'
import reactIcon from '../assets/images/react.png'
import vueIcon from '../assets/images/vue.png'
import sqlIcon from '../assets/images/sql.png'
import fbIcon from '../assets/images/firebase.png'
import gitIcon from '../assets/images/git.png'
const services = ref([
  {
    id: 1,
    icon: htmlIcon,
    name: 'HTML',
    href: 'https://developer.mozilla.org/en-US/docs/Web/HTML',
  },
  {
    id: 2,
    icon: cssIcon,
    name: 'CSS',
    href: 'https://developer.mozilla.org/en-US/docs/Web/CSS',
  },
  {
    id: 3,
    icon: jsIcon,
    name: 'Javascript',
    href: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript',
  },
  {
    id: 4,
    icon: phpIcon,
    name: 'PHP',
    href: 'https://www.php.net/',
  },
  {
    id: 5,
    icon: aspIcon,
    name: 'ASP.NET',
    href: 'https://dotnet.microsoft.com/en-us/apps/aspnet/mvc',
  },
  {
    id: 6,
    icon: btIcon,
    name: 'Bootstrap',
    href: 'https://getbootstrap.com/docs/5.0/getting-started/introduction/',
  },
  {
    id: 7,
    icon: tlIcon,
    name: 'Tailwind css',
    href: 'https://tailwindcss.com/',
  },
  {
    id: 8,
    icon: reactIcon,
    name: 'React js',
    href: 'https://react.dev/',
  },
  {
    id: 9,
    icon: vueIcon,
    name: 'Vue js',
    href: 'https://vuejs.org/',
  },
  {
    id: 10,
    icon: sqlIcon,
    name: 'SQL',
    href: 'https://www.w3schools.com/sql/sql_intro.asp',
  },
  {
    id: 11,
    icon: fbIcon,
    name: 'Firebase',
    href: 'https://firebase.google.com/',
  },
  {
    id: 12,
    icon: gitIcon,
    name: 'Git',
    href: 'https://www.git-scm.com/',
  },
])
</script>

<style scoped>
.hover-effect {
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
}

.hover-effect:hover {
  transform: translateY(-10px) scale(1.05);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.5);
  background-color: #1e2749;
}

.hover-effect:hover h3,
.hover-effect:hover p {
  color: #ffffff;
}
</style>
