<template>
  <div class="bg-[#111827] min-h-screen">
    <Navbar />
    <HeroSection />
    <Skills />
    <About />
    <Projects />
  </div>
</template>
<script setup>
import { defineAsyncComponent } from 'vue'
const Navbar = defineAsyncComponent(() => import('@/components/NavBar.vue'))
const HeroSection = defineAsyncComponent(
  () => import('@/components/HeroSection.vue'),
)
const Skills = defineAsyncComponent(() => import('@/components/Skills.vue'))
const About = defineAsyncComponent(() => import('@/components/AboutMe.vue'))
const Projects = defineAsyncComponent(
  () => import('@/components/ProjectSection.vue'),
)
</script>

<style scoped></style>
