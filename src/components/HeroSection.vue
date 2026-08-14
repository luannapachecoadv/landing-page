<template>
  <section class="relative w-full min-h-[600px] md:min-h-[707px] flex items-center overflow-hidden">
    <!-- Background image -->
    <div class="absolute inset-0 z-0">
      <picture>
        <source srcset="/src/assets/images/hero.webp" type="image/webp" />
        <img
          src="/src/assets/images/hero.jpg"
          alt="Escritório jurídico moderno com ambientação sofisticada"
          class="w-full h-full object-cover"
        />
      </picture>
      <!-- Navy overlay -->
      <div class="absolute inset-0" style="background-color: rgba(0, 13, 34, 0.45);"></div>
    </div>

    <!-- Content -->
    <div class="relative z-10 container-page w-full py-20 md:py-24">
      <div
        class="max-w-2xl p-8 md:p-12 border-l-4 shadow-2xl backdrop-blur-sm"
        style="background-color: rgba(255,255,255,0.08); border-color: var(--color-secondary);"
      >
        <!-- Label -->
        <span
          class="inline-block font-body text-xs font-semibold uppercase tracking-widest mb-6"
          style="color: var(--color-secondary-fixed-dim);"
        >Direito Médico &amp; da Saúde</span>

        <!-- Headline -->
        <h1 class="font-display font-bold text-3xl md:text-5xl leading-tight mb-6" style="color: #ffffff; letter-spacing: -0.02em;">
          Excelência e Ética no Direito Médico
        </h1>

        <!-- Subtitle -->
        <p class="font-body text-lg leading-relaxed mb-10" style="color: rgba(255,255,255,0.88);">
          Defesa especializada para profissionais da saúde e instituições hospitalares com foco em resultados e segurança jurídica.
        </p>

        <!-- CTA Buttons -->
        <div class="flex flex-col sm:flex-row gap-4">
          <a
            id="hero-cta-whatsapp"
            :href="whatsappUrl"
            target="_blank"
            rel="noopener noreferrer"
            class="font-body font-bold text-base py-4 px-8 rounded text-center transition-all hover:opacity-90 active:scale-95 shadow-lg"
            style="background-color: var(--color-primary); color: #ffffff;"
          >
            Agende uma Consulta
          </a>
          <a
            id="hero-cta-services"
            href="#services"
            class="font-body font-bold text-base py-4 px-8 rounded text-center border-2 transition-all hover:opacity-80 active:scale-95"
            style="border-color: var(--color-secondary-fixed); color: var(--color-secondary-fixed); background-color: transparent;"
          >
            Nossos Serviços
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const whatsappUrl = 'https://wa.me/5562996880352'
</script>
