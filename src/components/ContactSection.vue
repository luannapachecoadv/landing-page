<template>
  <section id="contact" class="py-24" style="background-color: var(--color-surface-container-lowest);">
    <div class="container-page">
      <!-- Section header -->
      <div class="text-center mb-16">
        <span
          class="font-body text-xs font-semibold uppercase tracking-widest mb-4 block"
          style="color: var(--color-secondary);"
        >Fale Conosco</span>
        <h2
          class="font-display font-bold text-3xl md:text-5xl mb-5"
          style="color: var(--color-primary); letter-spacing: -0.02em;"
        >Inicie sua Defesa</h2>
        <div class="w-20 h-1 mx-auto rounded-full" style="background-color: var(--color-secondary);"></div>
      </div>

      <!-- Content -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-12 md:gap-20 items-center">
        <!-- Left: info text -->
        <div class="space-y-6">
          <p class="font-body text-lg leading-relaxed" style="color: var(--color-on-surface-variant);">
            Estamos prontos para oferecer a segurança jurídica que sua prática profissional exige. Entre em contato pelo canal de sua preferência e nossa equipe retornará em até 24h.
          </p>

          <!-- Contact items -->
          <div class="space-y-5 mt-8">
            <a
              v-for="item in contacts"
              :key="item.id"
              :id="item.id"
              :href="item.href"
              :target="item.external ? '_blank' : undefined"
              :rel="item.external ? 'noopener noreferrer' : undefined"
              class="flex items-center gap-4 group"
            >
              <div
                class="p-3 rounded-full transition-colors"
                style="background-color: color-mix(in srgb, var(--color-secondary) 12%, transparent);"
              >
                <span
                  class="material-symbols-outlined transition-colors"
                  style="color: var(--color-secondary);"
                >{{ item.icon }}</span>
              </div>
              <div>
                <span
                  class="block font-body text-xs font-semibold uppercase tracking-widest mb-0.5"
                  style="color: var(--color-on-surface-variant);"
                >{{ item.label }}</span>
                <span
                  class="font-body text-base font-bold group-hover:opacity-80 transition-opacity"
                  style="color: var(--color-primary);"
                >{{ item.display }}</span>
              </div>
            </a>
          </div>
        </div>

        <!-- Right: CTA card -->
        <div
          class="p-10 rounded border ambient-shadow"
          style="background-color: var(--color-surface-container-low); border-color: color-mix(in srgb, var(--color-outline) 12%, transparent);"
        >
          <div class="text-center mb-8">
            <span class="material-symbols-outlined text-5xl mb-4 block" style="color: var(--color-secondary);">handshake</span>
            <h3 class="font-display font-semibold text-2xl mb-3" style="color: var(--color-primary);">
              Consulta Inicial
            </h3>
            <p class="font-body text-sm leading-relaxed" style="color: var(--color-on-surface-variant);">
              Apresente seu caso e receba uma avaliação jurídica especializada com agilidade e sigilo.
            </p>
          </div>

          <div class="flex flex-col gap-4">
            <a
              id="contact-cta-whatsapp"
              href="https://wa.me/5562996880352"
              target="_blank"
              rel="noopener noreferrer"
              class="font-body font-bold text-base py-4 px-8 rounded text-center transition-all hover:opacity-90 active:scale-95 shadow flex items-center justify-center gap-2"
              style="background-color: var(--color-primary); color: #ffffff;"
            >
              <span class="material-symbols-outlined text-xl">chat</span>
              Falar pelo WhatsApp
            </a>
            <a
              id="contact-cta-email"
              href="mailto:luannapachecoadv@gmail.com"
              class="font-body font-bold text-base py-4 px-8 rounded text-center border-2 transition-all hover:opacity-80 active:scale-95 flex items-center justify-center gap-2"
              style="border-color: var(--color-primary); color: var(--color-primary); background-color: transparent;"
            >
              <span class="material-symbols-outlined text-xl">mail</span>
              Enviar E-mail
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const contacts = [
  {
    id: 'contact-email',
    icon: 'mail',
    label: 'E-mail',
    display: 'luannapachecoadv@gmail.com',
    href: 'mailto:luannapachecoadv@gmail.com',
    external: false,
  },
  {
    id: 'contact-whatsapp',
    icon: 'phone',
    label: 'WhatsApp',
    display: '(62) 99688-0352',
    href: 'https://wa.me/5562996880352',
    external: true,
  },
]
</script>
