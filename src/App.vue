<script setup>
  import AOS from 'aos'
  import Header from './components/Header.vue';
  import { onMounted } from 'vue';
  import HeroSection from './components/HeroSection.vue';
  import EducationSection from './components/EducationSection.vue';
import Certification from './components/Certification.vue';
import About from './components/About.vue';
import Skills from './components/Skills.vue';
import Project from './components/Project.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';


  onMounted(() => {
    AOS.init({
      duration: 1000,
      once: false,
      offset: 100
    })
  })
</script>

<template>
  <Header/>
  <HeroSection />
  <EducationSection />
  <Certification />
  <About />
  <Skills />
  <Project />
  <Contact />
  <Footer />
</template>

<style scoped></style>
