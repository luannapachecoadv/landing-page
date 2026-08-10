<template>
  <section id="about" class="py-24 overflow-hidden" style="background-color: var(--color-primary);">
    <div class="container-page grid grid-cols-1 md:grid-cols-2 gap-12 md:gap-16 items-center">
      <!-- Image column -->
      <div class="relative flex justify-center md:justify-start">
        <!-- Decorative ring -->
        <div
          class="absolute -top-8 -left-8 w-40 h-40 rounded-full border-2 hidden md:block"
          style="border-color: color-mix(in srgb, var(--color-secondary) 30%, transparent);"
        ></div>
        <picture>
          <source srcset="/src/assets/images/about-me.webp" type="image/webp" />
          <img
            src="/src/assets/images/about-me.jpg"
            alt="Dra. Luanna Pacheco, advogada especialista em Direito Médico"
            class="relative z-10 w-full max-w-sm md:max-w-none h-auto md:h-[600px] object-cover rounded-sm shadow-2xl"
          />
        </picture>
      </div>

      <!-- Text column -->
      <div class="space-y-8">
        <span
          class="font-body text-xs font-semibold uppercase tracking-widest block"
          style="color: var(--color-secondary); letter-spacing: 0.2em;"
        >Trajetória e Propósito</span>

        <h2 class="font-display font-bold text-3xl md:text-5xl" style="color: #ffffff; letter-spacing: -0.02em;">
          Dra. Luanna Pacheco
        </h2>

        <div class="w-20 h-1 rounded-full" style="background-color: var(--color-secondary);"></div>

        <p class="font-body text-lg leading-relaxed" style="color: var(--color-surface-variant);">
          Especialista em Direito Médico e da Saúde, a Dra. Luanna Pacheco dedica sua carreira à proteção jurídica daqueles que dedicam suas vidas ao cuidado humano. Com uma abordagem que une rigor técnico e profunda empatia, ela se tornou referência na defesa da classe médica.
        </p>
        <p class="font-body text-lg leading-relaxed" style="color: var(--color-surface-variant);">
          Sua atuação é pautada na prevenção de litígios e na construção de um ambiente institucional seguro, permitindo que profissionais e hospitais foquem no que é essencial: a excelência no atendimento.
        </p>

        <!-- OAB badge -->
        <div
          class="inline-flex items-center gap-3 px-5 py-3 rounded border"
          style="border-color: color-mix(in srgb, var(--color-secondary) 40%, transparent); background-color: rgba(255,255,255,0.05);"
        >
          <span class="material-symbols-outlined" style="color: var(--color-secondary);">verified</span>
          <span class="font-body text-sm font-medium" style="color: rgba(255,255,255,0.85);">OAB/GO n.º 73.377</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>
