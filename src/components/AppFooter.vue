<template>
  <footer class="py-16 border-t" style="background-color: var(--color-primary); border-color: color-mix(in srgb, var(--color-outline) 10%, transparent);">
    <div class="container-page">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-10 mb-12">
        <!-- Brand -->
        <div class="md:col-span-1">
          <span class="font-display font-bold text-2xl tracking-tighter block mb-3" style="color: var(--color-on-primary);">
            LUANNA PACHECO
          </span>
          <p class="font-body text-sm leading-relaxed" style="color: var(--color-surface-variant);">
            Advocacia especializada em Direito Médico e da Saúde.<br />OAB/GO n.º 73.377.
          </p>
        </div>

        <!-- Quick links -->
        <div>
          <h4 class="font-body text-xs font-semibold uppercase tracking-widest mb-4" style="color: var(--color-secondary);">
            Navegação
          </h4>
          <ul class="space-y-3">
            <li v-for="link in navLinks" :key="link.href">
              <a
                :href="link.href"
                class="font-body text-sm transition-opacity hover:opacity-70"
                style="color: var(--color-surface-variant);"
              >{{ link.label }}</a>
            </li>
          </ul>
        </div>

        <!-- Social & contact -->
        <div>
          <h4 class="font-body text-xs font-semibold uppercase tracking-widest mb-4" style="color: var(--color-secondary);">
            Siga nas Redes
          </h4>
          <div class="flex gap-4">
            <a
              id="footer-instagram"
              href="https://www.instagram.com/luannastpacheco/"
              target="_blank"
              rel="noopener noreferrer"
              aria-label="Instagram de Luanna Pacheco"
              class="p-2.5 rounded transition-all hover:opacity-70 hover:scale-110 active:scale-95"
              style="color: var(--color-on-primary);"
            >
              <!-- Instagram SVG icon -->
              <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 1 0 0 12.324 6.162 6.162 0 0 0 0-12.324zM12 16a4 4 0 1 1 0-8 4 4 0 0 1 0 8zm6.406-11.845a1.44 1.44 0 1 0 0 2.881 1.44 1.44 0 0 0 0-2.881z"/>
              </svg>
            </a>
          </div>
        </div>
      </div>

      <!-- Divider -->
      <div class="border-t pt-8" style="border-color: color-mix(in srgb, var(--color-outline) 15%, transparent);">
        <p class="font-body text-xs text-center" style="color: color-mix(in srgb, var(--color-surface-variant) 70%, transparent);">
          © {{ currentYear }} Luanna Stéphany Gonçalves Pacheco. Todos os direitos reservados.
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
const currentYear = new Date().getFullYear()

const navLinks = [
  { href: '#services', label: 'Serviços' },
  { href: '#about', label: 'Sobre' },
  { href: '#contact', label: 'Contato' },
]
</script>
