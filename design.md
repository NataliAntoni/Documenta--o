# desing.md

# design.md

# Portal de Parcerias Netz

## Versão

1.0

---

# Objetivo

O Portal de Parcerias Netz tem como objetivo transformar o processo tradicional de coleta de requisitos em uma experiência interativa e intuitiva.

A interface utiliza conceitos de gamificação corporativa, navegação em carousel e feedback visual contínuo para reduzir a percepção de esforço do usuário durante o preenchimento do briefing do projeto.

A identidade visual é inspirada na marca Netz, adotando uma linguagem Dark Tech moderna e profissional.

---

# Identidade Visual

## Conceito

A interface deve transmitir:

- tecnologia;
- inovação;
- organização;
- inteligência artificial;
- confiabilidade;
- experiência guiada.

Evitar elementos excessivamente infantis ou lúdicos.

A gamificação deve aumentar o engajamento sem comprometer a seriedade do ambiente B2B.

---

# Paleta de Cores

## Primária

| Token | Valor |
| --- | --- |
| Primary | #B7F36B |
| Primary Hover | #A7ED5D |
| Primary Active | #5B8E20 |

Utilização:

- botões;
- barra de progresso;
- indicadores ativos;
- destaques;
- estados concluídos.

---

## Fundo

| Token | Valor |
| --- | --- |
| Background | #050505 |
| Surface | #101010 |
| Card | #151515 |
| Border | #1C1C1C |

---

## Texto

| Token | Valor |
| --- | --- |
| Text Primary | #F5F5F5 |
| Text Secondary | #B3B3B3 |
| Text Disabled | #666666 |

---

## Feedback

| Token | Valor |
| --- | --- |
| Success | #7AE33C |
| Warning | #FFC857 |
| Error | #FF5C5C |

---

# Tipografia

## Fonte Principal

Inter

Fallback:

sans-serif

---

## Hierarquia

### H1

48px

700

---

### H2

32px

600

---

### H3

24px

600

---

### Texto

16px

400

---

### Label

14px

500

---

### Botões

16px

600

---

# Grid

## Desktop

12 colunas

Margin:

80px

Gap:

24px

---

## Tablet

8 colunas

Gap:

20px

---

## Mobile

4 colunas

Gap:

16px

---

# Espaçamentos

Sistema baseado em múltiplos de 8.

4

8

16

24

32

48

64

96

---

# Bordas

## Cards

32px

---

## Botões

16px

---

## Inputs

12px

---

## Avatar

50%

---

# Sombras

## Glow Primário

rgba(183,243,107,.25)

Blur:

24px

---

## Cards

rgba(0,0,0,.35)

Blur:

32px

---

# Breakpoints

## Mobile

320px – 767px

---

## Tablet

768px – 1023px

---

## Notebook

1024px – 1439px

---

## Desktop

1440px+

---

# Componentes

## Botão Primário

Cor:

Primary

Texto:

Background

Radius:

16px

---

## Botão Secundário

Background:

Surface

Border:

Primary

Texto:

Primary

---

## Card

Background:

Card

Radius:

32px

Border:

1px solid Border

---

## Input

Background:

Surface

Radius:

12px

Border:

Border

Focus:

Primary

---

# Estrutura do Portal

O formulário é dividido em cinco grupos principais.

## Grupo 1

Empresa

---

## Grupo 2

Projeto

---

## Grupo 3

Objetivos

---

## Grupo 4

Funcionalidades

---

## Grupo 5

Planejamento

---

# Navegação

Cada grupo possui uma quantidade variável de blocos.

Cada bloco contém até quatro perguntas.

Fluxo:

Grupo

↓

Bloco

↓

Perguntas

↓

Próximo Bloco

↓

Próximo Grupo

---

# Carousel

O carousel representa a progressão do usuário.

## Bloco Atual

- centralizado;
- maior escala;
- destaque visual;
- totalmente opaco.

## Blocos Futuros

- posicionados ao fundo;
- escala reduzida;
- opacidade menor.

## Blocos Concluídos

- deslocados para trás;
- menor destaque;
- identificados como concluídos.

---

# Barra de Progresso

Existem dois níveis.

## Global

Mostra quantos grupos foram concluídos.

Exemplo:

2 de 5 grupos.

---

## Local

Mostra o progresso do grupo atual.

Exemplo:

3 de 6 blocos.

---

# Feedback Visual

Toda ação do usuário deve gerar resposta visual.

Estados:

- pendente;
- em andamento;
- concluído.

---

# Animações

## Hover

200ms

---

## Botões

300ms

---

## Carousel

400ms

Transform + Opacity

---

## Troca de Grupo

500ms

---

# Responsividade

Em dispositivos menores:

- reduzir espaçamentos;
- empilhar elementos;
- manter no máximo um bloco do carousel totalmente visível;
- preservar a barra de progresso.

---

# Princípios Visuais

## Jornada Guiada

O usuário deve sentir que está avançando em pequenas etapas.

---

## Gamificação Corporativa

O sistema deve incentivar a conclusão do briefing sem utilizar elementos infantis.

---

## Clareza

Cada tela deve possuir um objetivo principal.

---

## Feedback Constante

O usuário deve compreender o progresso do preenchimento.

---

## Consistência

Todos os componentes devem seguir o mesmo padrão visual.

---

## Inteligência Artificial

A interface deve comunicar que as informações fornecidas estão sendo utilizadas para estruturar automaticamente o briefing do projeto.

---

# Experiência do Usuário

O Portal de Parcerias Netz não deve ser percebido como um formulário tradicional.

A experiência proposta consiste em uma jornada de construção de briefing, na qual o usuário avança por grupos e blocos de perguntas enquanto acompanha visualmente sua evolução até a conclusão do projeto.