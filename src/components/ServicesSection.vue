<template>
  <section id="services" class="py-24" style="background-color: var(--color-background);">
    <div class="container-page">
      <!-- Section header -->
      <div class="text-center mb-16">
        <span
          class="font-body text-xs font-semibold uppercase tracking-widest mb-4 block"
          style="color: var(--color-secondary);"
        >Atuação Especializada</span>
        <h2
          class="font-display font-bold text-3xl md:text-5xl mb-5"
          style="color: var(--color-primary); letter-spacing: -0.02em;"
        >Especialidades Jurídicas</h2>
        <div class="w-20 h-1 mx-auto rounded-full" style="background-color: var(--color-secondary);"></div>
      </div>

      <!-- Cards grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <article
          v-for="service in services"
          :key="service.id"
          :id="`service-${service.id}`"
          class="group bg-white p-8 border border-t-2 ambient-shadow transition-all duration-300 hover:shadow-xl hover:-translate-y-1 cursor-default"
          style="border-color: color-mix(in srgb, var(--color-outline) 10%, transparent); border-top-color: var(--color-secondary);"
        >
          <div
            class="mb-6 transition-transform duration-300 group-hover:scale-110"
            style="color: var(--color-primary);"
          >
            <span class="material-symbols-outlined text-4xl">{{ service.icon }}</span>
          </div>
          <h3
            class="font-display font-semibold text-xl md:text-2xl mb-4 leading-snug"
            style="color: var(--color-primary);"
          >{{ service.title }}</h3>
          <p
            class="font-body text-sm leading-relaxed"
            style="color: var(--color-on-surface-variant);"
          >{{ service.description }}</p>
          <ul
            v-if="service.items"
            class="mt-4 space-y-1.5"
            style="color: var(--color-on-surface-variant);"
          >
            <li
              v-for="item in service.items"
              :key="item"
              class="font-body text-sm leading-relaxed flex gap-2"
            >
              <span class="mt-0.5 shrink-0 material-symbols-outlined text-base" style="color: var(--color-secondary);">chevron_right</span>
              <span>{{ item }}</span>
            </li>
          </ul>
        </article>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    id: 'crm',
    icon: 'balance',
    title: 'Defesa em Processos Éticos (CRM)',
    description:
      'Atuação estratégica perante os conselhos profissionais, garantindo o direito à ampla defesa e preservação da reputação.',
  },
  {
    id: 'civil',
    icon: 'medical_information',
    title: 'Responsabilidade Civil Médica',
    description:
      'Defesa técnica em ações de indenização por erro médico, danos morais e materiais com foco na perícia judicial.',
  },
  {
    id: 'compliance',
    icon: 'domain_verification',
    title: 'Consultoria em Compliance Hospitalar',
    description:
      'Implementação de protocolos de segurança, gestão de riscos e adequação às normas vigentes da ANS e ANVISA.',
  },
  {
    id: 'bioetica',
    icon: 'clinical_notes',
    title: 'Assessoria em Bioética',
    description:
      'Pareceres jurídicos sobre questões éticas complexas, diretivas antecipadas de vontade e comitês de ética em pesquisa.',
  },
  {
    id: 'loas',
    icon: 'diversity_3',
    title: 'LOAS para Autistas e TDAH',
    description:
      'Orientação e atuação jurídica especializada na obtenção do Benefício de Prestação Continuada (BPC/LOAS) para crianças e adultos com Autismo (TEA) e TDAH.',
  },
  {
    id: 'planos',
    icon: 'health_and_safety',
    title: 'Ações Contra Planos de Saúde',
    description: 'Atuamos na defesa dos direitos dos beneficiários frente a práticas abusivas das operadoras, incluindo:',
    items: [
      'Recusa injustificada de exames, cirurgias, internações ou tratamentos indispensáveis à saúde do beneficiário;',
      'Reajustes abusivos da mensalidade, sobretudo em contratos de idosos ou de pessoas com doenças crônicas;',
      'Cancelamento unilateral ou indevido do plano de saúde;',
      'Negativa de reembolso de despesas médicas garantidas em contrato;',
      'Exclusão de hospitais ou médicos da rede credenciada sem comunicação prévia ao beneficiário;',
      'Falta de cobertura para home care ou remoção por ambulância quando clinicamente necessários.',
    ],
  },
  {
    id: 'trabalhista',
    icon: 'groups',
    title: 'Direitos dos Profissionais da Saúde',
    description:
      'Médicos, enfermeiros, técnicos e demais profissionais da saúde enfrentam rotinas exaustivas, plantões excessivos e, muitas vezes, direitos trabalhistas desrespeitados. Atuamos exclusivamente na defesa desses profissionais, com conhecimento aprofundado das particularidades da categoria. Nosso compromisso é garantir que quem cuida da saúde dos outros também tenha seus direitos protegidos, com atendimento humanizado e atuação estratégica em negociações extrajudiciais e ações judiciais.',
    items: [
      'Horas extras e jornada em regime de plantão;',
      'Adicional de insalubridade e periculosidade;',
      'Assédio moral e ambiente de trabalho hostil;',
      'Rescisão indireta e verbas rescisórias;',
      'Reconhecimento de vínculo empregatício;',
      'Equiparação salarial e desvio de função.',
    ],
  },
]
</script>
