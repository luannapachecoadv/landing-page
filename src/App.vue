<template>
  <AppHeader />
  <main>
    <HeroSection />
    <ServicesSection />
    <AboutSection />
    <ContactSection />
  </main>
  <AppFooter />
</template>

<script setup>
import AppHeader from './components/AppHeader.vue'
import HeroSection from './components/HeroSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import AboutSection from './components/AboutSection.vue'
import ContactSection from './components/ContactSection.vue'
import AppFooter from './components/AppFooter.vue'
</script>
