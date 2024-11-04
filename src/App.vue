<template>
  <div class="bg-[#111827] min-h-screen">
    <Suspense>
      <template #default>
        <div>
          <Navbar />
          <HeroSection />
          <Skills />
          <Projects />
          <About />
          <Contact />
          <Footer />
          <BackToTop />
        </div>
      </template>
      <template #fallback>
        <div class="flex justify-center items-center min-h-screen">
          <LoadingSpinner />
        </div>
      </template>
    </Suspense>
  </div>
</template>
<script setup>
import { defineAsyncComponent } from 'vue'
import LoadingSpinner from './components/LoadingSpinner.vue'
const Navbar = defineAsyncComponent(() => import('@/components/NavBar.vue'))
const HeroSection = defineAsyncComponent(
  () => import('@/components/HeroSection.vue'),
)
const Skills = defineAsyncComponent(() => import('@/components/Skills.vue'))
const About = defineAsyncComponent(() => import('@/components/AboutMe.vue'))
const Contact = defineAsyncComponent(
  () => import('@/components/ContactSection.vue'),
)
const Projects = defineAsyncComponent(
  () => import('@/components/ProjectSection.vue'),
)
const Footer = defineAsyncComponent(() => import('@/components/Footer.vue'))
const BackToTop = defineAsyncComponent(
  () => import('@/components/BackToTop.vue'),
)
</script>

<style scoped></style>
