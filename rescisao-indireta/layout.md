# Layout: Método Rescisão Segura

Este documento contém a bíblia de design para a página de Rescisão Indireta.

## Diretrizes Gerais
- **Paleta de Cores**:
  - Navy: `#0A192F` (Acentos e Contrastes)
  - Light Gray: `#F0F2F5` (Fundo sutil)
  - Gold: `#B8860B` (Primária de ação)
  - Gold Hover: `#996515`
  - White: `#FFFFFF` (Fundo principal)
- **Tipografia**:
  - Títulos: Playfair Display (Serif) - Pesos 700 e 900
  - Corpo: Inter (Sans) - Pesos 400 e 700
- **Efeito Principal**: Glassmorphism (Glass-Blur-12px, border-gold-30%)

---

## Seção 1: Hero (Existente)
- **Arquetipo**: Split Vertical (Assimétrico)
- **Constraints**: Glassmorphism + Image Overlay
- **Justificativa**: Transmite modernidade e clareza imediata.
- **Layout**: 1.2fr (Texto) e 0.8fr (Imagem)

## Seção 2: Identificação - A Dor (Existente)
- **Arquetipo**: Bento Grid (Organizado)
- **Constraints**: Glass Cards + Hover Lift
- **Justificativa**: Organiza dores complexas em pílulas de fácil leitura.

---

## Seção 3: O Mecanismo Único - A Solução

### Arquetipo e Constraints
- **Arquetipo**: Split Diagonal (Broken Layout)
- **Constraints**: Clip-path Section + Text Reveal
- **Justificativa**: O corte diagonal simboliza a ruptura com o ambiente tóxico. O "Text Reveal" dá peso às palavras do TST.

### Conteúdo
- Título: A Rescisão Indireta: A "Justa Causa" aplicada ao patrão.
- Corpo: Muitos acreditam que a única forma de sair de uma empresa ruim é pedindo as contas e perdendo tudo. Mas a lei protege o bom profissional. Quando a empresa descumpre o contrato, você tem o direito de "demitir" a empresa.
- Destaque: O TST (Tribunal Superior do Trabalho) já consolidou: a falta de recolhimento de FGTS, por si só, é motivo suficiente para você sair IMEDIATAMENTE com todos os seus direitos garantidos. Saia de cabeça erguida, com o bolso cheio e sua reputação intacta.

### Layout
- Background: `#0A192F` (Navy fundo) com `clip-path: polygon(0 0, 100% 5%, 100% 95%, 0 100%)`.
- Padding: `160px 0`.
- Split: Conteúdo à esquerda (60%), Elemento decorativo legal à direita (40% - Ícone de Martelo do Juiz estilizado em Gold ou Overlay de documento).

### Tipografia
- Título: `clamp(2rem, 5vw, 3.5rem)`, color: `#FFFFFF`.
- Corpo: `1.2rem`, color: `rgba(255,255,255,0.8)`, line-height: 1.6.

### Cores
- Fundo: `#0A192F`.
- Texto Principal: `#FFFFFF`.
- Acento: `#B8860B`.

### Elementos Visuais
- Uma linha fina em gradiente gold (horizontal) separando o título do texto.
- Efeito de "Glow" sutil no centro da seção.

### Animações
- `data-aos="fade-right"` no título.
- `Text Reveal` (letra por letra) no parágrafo de destaque do TST usando `IntersectionObserver`.

### Interatividade
- Hover no parágrafo do TST aumenta levemente a brilho do texto (`color: #FFFFFF`).

---

## Seção 4: Arquitetura do Produto - O Método

### Arquetipo e Constraints
- **Arquetipo**: Modular (Cartões Verticais)
- **Constraints**: Scroll Progress + Stagger + Progress Bar Linear
- **Justificativa**: Uma jornada precisa de clareza nas etapas. O scroll progress visualiza o avanço.

### Conteúdo
- Título: Método Rescisão Segura: Sua Jornada de Libertação com Segurança Financeira.
- Itens:
    1. **Auditoria de Viabilidade**: Analisamos seus documentos (FGTS, holerites, mensagens) antes de qualquer ação. Só seguimos se a prova for robusta.
    2. **Blindagem de Provas**: Protocolo de coleta de evidências digitais via blockchain ou ata notarial, sem que a empresa perceba.
    3. **Estratégia de Transição**: Orientamos o momento exato do afastamento para evitar alegação de abandono e garantir o seguro-desemprego.
    4. **Cálculo de Liquidez**: Você recebe uma projeção detalhada de quanto vai receber (Verbas + FGTS + Multa + Danos Morais).

### Layout
- Container Central (`800px` max).
- Itens em lista vertical com `border-left` dinâmico que "carrega" com o scroll.
- Espaçamento entre itens: `60px`.

### Tipografia
- Título Principal: `clamp(2rem, 4vw, 3rem)`, margin-bottom: `4rem`.
- Título Item: `1.5rem`, font-weight: 700.
- Texto Item: `1.1rem`, color: var(--text-dim).

### Cores
- Barra de Progresso Lateral: Gradiente `#B8860B` para `#0A192F`.
- Card Item (on active): Background sutil `rgba(184, 134, 11, 0.05)`.

### Animações
- Barra de progresso lateral cresce conforme a seção é scrollada (`height: 0` a `100%`).
- Itens ganham opacidade e escala (`scale(0.95)` a `scale(1)`) quando entram no viewport.

---

## Seção 5: Autoridade e Prova Social

### Arquetipo e Constraints
- **Arquetipo**: Editorial (Clean)
- **Constraints**: Negative Margin + Floating Element
- **Justificativa**: Transmite seriedade e leveza.

### Conteúdo
- Título: Especialistas em Direito do Trabalho com Foco em Rescisão Indireta.
- Bullets:
    - +10 anos de atuação específica.
    - Centenas de profissionais libertos de ambientes tóxicos.
    - Atendimento humanizado e sigiloso, respeitando o Código de Ética da OAB.

### Layout
- Flex 1:1. 
- Lado esquerdo: Card de destaque com números grandes (+10, Centenas).
- Lado direito: Texto explicativo e selo de "Sigilo OAB".
- Negative margin no card da esquerda para sobrepor levemente a seção anterior.

### Cores
- Background: `#FFFFFF`.
- Card de números: Glassmorphism com fundo Navy `#0A192F`.

### Animações
- `counter-up` nos números (+10, Centenas).
- Float suave no "Selo OAB".

---

## Seção 6: FAQ - Quebra de Objeções

### Arquetipo e Constraints
- **Arquetipo**: Contained Center
- **Constraints**: Accordion (Custom Stylized) + Hover Glow
- **Justificativa**: Foco total na dúvida do usuário, evitando distrações.

### Conteúdo
- Perguntas: 
    1. Vou ficar com o nome sujo?
    2. E se eu não tiver provas?
    3. Quanto tempo demora?
- Respostas da copy.

### Layout
- Container estreito (`700px`).
- Accordion com ícones de `+` e `-` que rotacionam.

### Cores
- Border: `1px solid var(--glass-border)`.
- Fundo expansivo: `var(--primary-light)`.

### Interatividade
- Glow dourado sutil no hover das perguntas.

---

## Seção 7: Footer & CTA Final (O Formulário)

### Arquetipo e Constraints
- **Arquetipo**: Spotlight (Focus on Form)
- **Constraints**: Mesh Gradient Background + Glassmorphism
- **Justificativa**: O objetivo final é a captura do lead. O spotlight foca a atenção no formulário.

### Conteúdo
- Headline: Comece sua jornada de libertação hoje mesmo.
- Subheadline: Preencha o formulário para uma avaliação sigilosa.
- **Formulário** (Regras da Skill Forms):
    - Campo Nome
    - Campo Email
    - Campo Telefone (intl-tel-input)
    - Botão: ENVIAR AVALIAÇÃO AGORA

### Layout
- Section Full Height ou `80vh`.
- Background animado (Mesh Gradient) em tons de Navy e Gold (muito sutil).
- Card central de formulário com Glassmorphism pesado (`blur(20px)`).

### Cores
- Headline: `#FFFFFF`.
- Input borders: Gold 30%.

### Interatividade
- Botão CTA pulsando levemente (Glow pulse).

---
