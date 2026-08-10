<template>
  <header
    class="sticky top-0 z-50 w-full border-b backdrop-blur-md transition-shadow"
    :class="scrolled ? 'shadow-md' : 'shadow-sm'"
    style="background-color: color-mix(in srgb, var(--color-surface) 90%, transparent); border-color: color-mix(in srgb, var(--color-outline) 20%, transparent);"
  >
    <div class="container-page flex items-center justify-between h-20">
      <!-- Logo -->
      <a href="#" class="font-display font-bold tracking-tighter text-2xl md:text-3xl" style="color: var(--color-primary);">
        LUANNA PACHECO
      </a>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center gap-8">
        <a
          href="#services"
          class="font-body text-sm font-medium transition-colors hover:opacity-80"
          style="color: var(--color-on-surface-variant);"
        >Serviços</a>
        <a
          href="#about"
          class="font-body text-sm font-medium transition-colors hover:opacity-80"
          style="color: var(--color-on-surface-variant);"
        >Sobre</a>
        <a
          href="#contact"
          class="font-body text-sm font-semibold py-2.5 px-6 rounded transition-all hover:opacity-80 active:scale-95"
          style="background-color: var(--color-primary); color: var(--color-on-primary);"
        >Contato</a>
      </nav>

      <!-- Mobile hamburger -->
      <button
        id="mobile-menu-btn"
        class="md:hidden p-2 rounded transition-colors"
        :aria-expanded="mobileOpen"
        aria-label="Abrir menu"
        @click="mobileOpen = !mobileOpen"
        style="color: var(--color-on-surface);"
      >
        <span class="material-symbols-outlined text-2xl">{{ mobileOpen ? 'close' : 'menu' }}</span>
      </button>
    </div>

    <!-- Mobile Drawer -->
    <Transition name="slide-down">
      <nav
        v-if="mobileOpen"
        id="mobile-menu"
        class="md:hidden border-t px-4 py-6 flex flex-col gap-4"
        style="background-color: var(--color-surface); border-color: color-mix(in srgb, var(--color-outline) 15%, transparent);"
      >
        <a
          href="#services"
          class="font-body text-base font-medium py-2 transition-colors"
          style="color: var(--color-on-surface-variant);"
          @click="mobileOpen = false"
        >Serviços</a>
        <a
          href="#about"
          class="font-body text-base font-medium py-2 transition-colors"
          style="color: var(--color-on-surface-variant);"
          @click="mobileOpen = false"
        >Sobre</a>
        <a
          href="#contact"
          class="font-body text-base font-semibold py-3 px-6 rounded text-center transition-all active:scale-95 mt-2"
          style="background-color: var(--color-primary); color: var(--color-on-primary);"
          @click="mobileOpen = false"
        >Contato</a>
      </nav>
    </Transition>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const mobileOpen = ref(false)
const scrolled = ref(false)

function handleScroll() {
  scrolled.value = window.scrollY > 20
}

onMounted(() => window.addEventListener('scroll', handleScroll))
onUnmounted(() => window.removeEventListener('scroll', handleScroll))
</script>

<style scoped>
.slide-down-enter-active,
.slide-down-leave-active {
  transition: all 0.25s ease;
}
.slide-down-enter-from,
.slide-down-leave-to {
  opacity: 0;
  transform: translateY(-8px);
}
</style>
