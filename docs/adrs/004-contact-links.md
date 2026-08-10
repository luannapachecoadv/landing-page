# ADR-004: Contato — Links Diretos (sem formulário)

| Campo      | Valor                  |
|------------|------------------------|
| Data       | 2026-08-09             |
| Status     | Aceito                 |
| Decisores  | Equipe de desenvolvimento |

## Contexto

O HTML original continha um formulário de contato (`<form>`). Sites estáticos hospedados no GitHub Pages não possuem backend para processar envio de formulários.

## Decisão

Substituir o formulário por **hyperlinks diretos** para WhatsApp (`https://wa.me/`) e e-mail (`mailto:`).

## Justificativa

- Elimina dependência de serviços terceiros (Formspree, EmailJS, etc.).
- Zero custo adicional e zero manutenção.
- UX mais direta para o público-alvo (profissionais de saúde em busca de contato rápido).
- WhatsApp é o canal de comunicação predominante no Brasil para contato profissional.
- Compatível com mobile-first: toca no link → abre o app diretamente.

## Consequências

- O formulário HTML foi removido da `ContactSection`.
- Os dados de contato exibidos:
  - **E-mail**: `luannapachecoadv@gmail.com` (link `mailto:`)
  - **WhatsApp**: número a ser preenchido futuramente (link `https://wa.me/`)
- A seção de contato mantém a identidade visual com cards de ícones e CTA.
