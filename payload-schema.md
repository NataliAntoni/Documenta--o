# Payload Schema do Formulário de Briefing

## Objetivo

Este documento define padrões para estruturação, nomenclatura e tipagem dos dados coletados pelo formulário de briefing do Portal de Parcerias.

Seu objetivo é garantir consistência na organização das informações, facilitar futuras integrações e servir como referência para processamento automatizado dos dados coletados.

---

## Escopo

Este documento não define:

* estrutura de banco de dados;
* endpoints de API;
* arquitetura backend;
* implementação específica em CMS.

Seu foco está na organização lógica das informações coletadas pelo formulário de briefing.

---

## O que é um payload

Payload é o conjunto de informações enviadas ou armazenadas após o preenchimento do formulário.

Exemplo:

```json
{
  "companyName": "Empresa Exemplo",
  "projectName": "Portal Institucional",
  "responsibleName": "João Silva"
}
```

Neste exemplo, cada campo representa uma informação fornecida pelo usuário durante o preenchimento do briefing.

---

## O que é um schema

Schema representa a definição da estrutura esperada dos dados.

Ele estabelece:

* quais campos existem;
* quais tipos de dados são aceitos;
* como os campos devem ser nomeados;
* como as informações devem ser organizadas.

---

# Convenções de nomenclatura

## Padrão adotado

Os campos deverão utilizar o padrão camelCase.

Exemplos:

```text
companyName
projectName
responsibleName
projectGoal
targetAudience
```

---

## Evitar

Não utilizar:

```text
CompanyName
PROJECT_NAME
nome_empresa
NomeEmpresa
```

---

## Regras gerais

* utilizar nomes em inglês;
* utilizar termos claros e descritivos;
* evitar abreviações desnecessárias;
* manter consistência em todos os campos;
* utilizar singular sempre que possível.

---

# Tipos de dados

Os campos poderão utilizar os seguintes tipos básicos.

---

## String

Utilizada para textos curtos ou longos.

Exemplos:

```text
companyName
email
projectGoal
services
```

Exemplo:

```json
{
  "companyName": "Empresa Exemplo"
}
```

---

## Boolean

Representa respostas de verdadeiro ou falso.

Exemplos:

```text
hasCMS
needsSEO
hasBlog
needsTraining
```

Exemplo:

```json
{
  "needsSEO": true
}
```

---

## Number

Representa valores numéricos.

Exemplos:

```text
approvalParticipants
estimatedUsers
```

Exemplo:

```json
{
  "approvalParticipants": 3
}
```

---

## Array

Representa listas de valores.

Exemplos:

```text
functionalities
references
integrations
```

Exemplo:

```json
{
  "functionalities": [
    "login",
    "dashboard",
    "payments"
  ]
}
```

---

## Object

Representa agrupamentos de informações relacionadas.

Exemplo:

```json
{
  "contact": {
    "responsibleName": "João Silva",
    "email": "joao@email.com",
    "phone": "(51) 99999-9999"
  }
}
```

---

# Estrutura geral proposta

Os dados poderão ser organizados seguindo a mesma divisão das etapas do formulário.

Exemplo:

```text
initialInformation
companyInformation
projectObjectives
targetAudience
projectType
structure
functionalities
content
design
references
cms
marketing
integrations
timeline
additionalQuestions
finalNotes
approvalProcess
postLaunch
```

Essa organização facilita manutenção, leitura e futura evolução do projeto.

---

# Princípios de modelagem

Durante a criação dos campos, recomenda-se:

* manter nomenclatura consistente;
* evitar duplicação de informações;
* utilizar tipos adequados para cada dado;
* priorizar clareza dos nomes;
* organizar os campos conforme a estrutura do formulário;
* permitir expansão futura sem necessidade de grandes alterações.

---

# Relação com o formulário de briefing

Cada pergunta existente no formulário deverá possuir um campo correspondente dentro do payload.

A estrutura documentada neste arquivo servirá como referência para organização dos dados coletados ao longo das 18 etapas do briefing.

As próximas seções apresentarão os campos previstos para cada etapa do formulário.

---

# Etapa 1 — Informações iniciais

## Grupo

```text
initialInformation
```

---

### companyName

**Tipo:** string

**Obrigatório:** sim

**Descrição:** nome da empresa cliente.

---

### projectName

**Tipo:** string

**Obrigatório:** sim

**Descrição:** nome utilizado para identificar o projeto.

---

### responsibleName

**Tipo:** string

**Obrigatório:** sim

**Descrição:** responsável principal pelo preenchimento do briefing.

---

### email

**Tipo:** string

**Obrigatório:** sim

**Descrição:** e-mail de contato do responsável.

---

### phone

**Tipo:** string

**Obrigatório:** sim

**Descrição:** telefone de contato.

---

### website

**Tipo:** string

**Obrigatório:** não

**Descrição:** endereço do site atual da empresa.

---

### socialMedia

**Tipo:** string

**Obrigatório:** não

**Descrição:** redes sociais da empresa.

---

### businessArea

**Tipo:** string

**Obrigatório:** sim

**Descrição:** segmento ou área de atuação.

---

### location

**Tipo:** string

**Obrigatório:** não

**Descrição:** cidade e país de atuação.

---

# Etapa 2 — Sobre a empresa

## Grupo

```text
companyInformation
```

---

### companyDescription

**Tipo:** string

**Obrigatório:** sim

**Descrição:** descrição geral da empresa.

---

### services

**Tipo:** string

**Obrigatório:** sim

**Descrição:** produtos ou serviços oferecidos.

---

### diferencial

**Tipo:** string

**Obrigatório:** não

**Descrição:** diferenciais competitivos relevantes.

---

### brandPerception

**Tipo:** string

**Obrigatório:** não

**Descrição:** percepção desejada da marca.

---

### brandInformation

**Tipo:** string

**Obrigatório:** não

**Descrição:** informações adicionais relacionadas à marca.

---

# Etapa 3 — Objetivo do projeto

## Grupo

```text
projectObjectives
```

---

### projectGoal

**Tipo:** string

**Obrigatório:** sim

**Descrição:** principal objetivo do projeto.

---

### projectProblem

**Tipo:** string

**Obrigatório:** sim

**Descrição:** problema que o projeto pretende resolver.

---

### expectedResults

**Tipo:** string

**Obrigatório:** não

**Descrição:** resultados esperados pelo cliente.

---

### projectPurposes

**Tipo:** array

**Obrigatório:** sim

**Descrição:** finalidades principais do projeto.

---

### Valores possíveis

```text
presentCompany
captureLeads
sell
automateProcesses
promoteBrand
provideInformation
other
```

---

# Etapa 4 — Público-alvo

## Grupo

```text
targetAudience
```

---

### primaryAudience

**Tipo:** string

**Obrigatório:** sim

**Descrição:** público principal do projeto.

---

### audienceType

**Tipo:** string

**Obrigatório:** sim

**Descrição:** classificação B2B ou B2C.

---

### audienceProfile

**Tipo:** string

**Obrigatório:** não

**Descrição:** perfil específico do público.

---

### ageRange

**Tipo:** string

**Obrigatório:** não

**Descrição:** faixa etária predominante.

---

### audienceNeeds

**Tipo:** string

**Obrigatório:** não

**Descrição:** necessidades importantes do público.

---

# Etapa 5 — Tipo de projeto

## Grupo

```text
projectType
```

---

### mainProjectType

**Tipo:** string

**Obrigatório:** sim

**Descrição:** classificação principal do projeto.

---

### Valores possíveis

```text
institutionalWebsite
portfolio
landingPage
portal
dashboard
internalSystem
platform
blog
ecommerce
other
```

---

# Exemplo da estrutura até a Etapa 5

```json
{
  "initialInformation": {
    "companyName": "",
    "projectName": "",
    "responsibleName": "",
    "email": "",
    "phone": "",
    "website": "",
    "socialMedia": "",
    "businessArea": "",
    "location": ""
  },

  "companyInformation": {
    "companyDescription": "",
    "services": "",
    "diferencial": "",
    "brandPerception": "",
    "brandInformation": ""
  },

  "projectObjectives": {
    "projectGoal": "",
    "projectProblem": "",
    "expectedResults": "",
    "projectPurposes": []
  },

  "targetAudience": {
    "primaryAudience": "",
    "audienceType": "",
    "audienceProfile": "",
    "ageRange": "",
    "audienceNeeds": ""
  },

  "projectType": {
    "mainProjectType": ""
  }
}
```
---

# Etapa 6 — Estrutura geral

## Grupo

```text id="e6-group"
structure
```

---

### pagesAndSections

**Tipo:** string

**Obrigatório:** sim

**Descrição:** páginas ou seções previstas para o projeto.

---

### hasSiteMap

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** indica se existe mapa do site definido.

---

### hasDefinedFlow

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** indica se existe fluxo de navegação previamente definido.

---

### hasRestrictedArea

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** informa se haverá área restrita para usuários.

---

### mainUserAction

**Tipo:** string

**Obrigatório:** sim

**Descrição:** principal ação que o usuário deverá executar.

---

### userJourney

**Tipo:** string

**Obrigatório:** não

**Descrição:** jornada esperada do usuário dentro do projeto.

---

# Etapa 7 — Funcionalidades

## Grupo

```text id="e7-group"
functionalities
```

---

### selectedFunctionalities

**Tipo:** array

**Obrigatório:** não

**Descrição:** funcionalidades selecionadas para o projeto.

---

### Valores possíveis

```text id="e7-values"
login
userArea
forms
upload
dashboard
adminPanel
chat
whatsappIntegration
payments
api
search
notifications
downloads
other
```

---

### functionalityDetails

**Tipo:** object

**Obrigatório:** não

**Descrição:** detalhes adicionais relacionados às funcionalidades selecionadas.

---

### Exemplo

```json id="e7-example"
{
  "selectedFunctionalities": [
    "login",
    "payments",
    "api"
  ],

  "functionalityDetails": {
    "payments": "Stripe",
    "api": "Integração com ERP"
  }
}
```

---

# Etapa 8 — Conteúdo

## Grupo

```text id="e8-group"
content
```

---

### hasContentReady

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** indica se já existe conteúdo pronto.

---

### existingMaterials

**Tipo:** string

**Obrigatório:** não

**Descrição:** materiais já disponíveis.

---

### textProvider

**Tipo:** string

**Obrigatório:** não

**Descrição:** responsável pelo fornecimento dos textos.

---

### imageProvider

**Tipo:** string

**Obrigatório:** não

**Descrição:** responsável pelo fornecimento das imagens.

---

### needsCopywriting

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** necessidade de produção de conteúdo textual.

---

### hasBlog

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** indica se haverá blog ou notícias.

---

### contentUpdateFrequency

**Tipo:** string

**Obrigatório:** não

**Descrição:** frequência prevista de atualização dos conteúdos.

---

# Etapa 9 — Design e identidade

## Grupo

```text id="e9-group"
design
```

---

### hasVisualIdentity

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** informa se a empresa possui identidade visual definida.

---

### hasLogo

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** indica existência de logotipo.

---

### hasBrandManual

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** informa se existe manual da marca.

---

### brandColors

**Tipo:** string

**Obrigatório:** não

**Descrição:** cores utilizadas pela marca.

---

### brandFonts

**Tipo:** string

**Obrigatório:** não

**Descrição:** tipografias utilizadas pela marca.

---

### visualStyle

**Tipo:** array

**Obrigatório:** não

**Descrição:** estilos visuais desejados para o projeto.

---

### Valores possíveis

```text id="e9-values"
modern
minimalist
sophisticated
technological
corporate
young
premium
other
```

---

# Etapa 10 — Referências

## Grupo

```text id="e10-group"
references
```

---

### favoriteWebsites

**Tipo:** string

**Obrigatório:** não

**Descrição:** sites que servem como referência para o cliente.

---

### competitors

**Tipo:** string

**Obrigatório:** não

**Descrição:** concorrentes relevantes.

---

### visualReferences

**Tipo:** string

**Obrigatório:** não

**Descrição:** referências visuais desejadas.

---

### uxReferences

**Tipo:** string

**Obrigatório:** não

**Descrição:** referências relacionadas à experiência do usuário.

---

### likedElements

**Tipo:** string

**Obrigatório:** não

**Descrição:** aspectos positivos identificados nas referências.

---

### avoidedElements

**Tipo:** string

**Obrigatório:** não

**Descrição:** elementos que o cliente prefere evitar.

---

# Exemplo da estrutura até a Etapa 10

```json id="e10-example"
{
  "structure": {
    "pagesAndSections": "",
    "hasSiteMap": false,
    "hasDefinedFlow": false,
    "hasRestrictedArea": false,
    "mainUserAction": "",
    "userJourney": ""
  },

  "functionalities": {
    "selectedFunctionalities": [],
    "functionalityDetails": {}
  },

  "content": {
    "hasContentReady": false,
    "existingMaterials": "",
    "textProvider": "",
    "imageProvider": "",
    "needsCopywriting": false,
    "hasBlog": false,
    "contentUpdateFrequency": ""
  },

  "design": {
    "hasVisualIdentity": false,
    "hasLogo": false,
    "hasBrandManual": false,
    "brandColors": "",
    "brandFonts": "",
    "visualStyle": []
  },

  "references": {
    "favoriteWebsites": "",
    "competitors": "",
    "visualReferences": "",
    "uxReferences": "",
    "likedElements": "",
    "avoidedElements": ""
  }
}
```
---

# Etapa 11 — Conteúdo dinâmico / CMS

## Grupo

```text id="e11-group"
cms
```

---

### canEditContent

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** informa se o cliente poderá editar conteúdos após a entrega.

---

### editableContent

**Tipo:** string

**Obrigatório:** não

**Descrição:** conteúdos que poderão ser editados pelo cliente.

---

### needsAdminPanel

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** indica necessidade de painel administrativo.

---

### updateResponsible

**Tipo:** string

**Obrigatório:** não

**Descrição:** responsável pelas atualizações de conteúdo.

---

### needsTraining

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** indica necessidade de treinamento.

---

### autonomyLevel

**Tipo:** string

**Obrigatório:** não

**Descrição:** nível de autonomia desejado pelo cliente.

---

### Valores possíveis

```text id="e11-values"
full
partial
none
```

---

# Etapa 12 — Marketing

## Grupo

```text id="e12-group"
marketing
```

---

### needsSEO

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** indica necessidade de otimização para mecanismos de busca.

---

### hasMarketingBlog

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** informa se haverá blog com foco em marketing de conteúdo.

---

### needsAnalytics

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** necessidade de ferramentas de análise.

---

### usesPixel

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** utilização de pixels de rastreamento.

---

### hasNewsletter

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** necessidade de newsletter.

---

### campaignIntegration

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** integração com campanhas de marketing.

---

### seoKeywords

**Tipo:** string

**Obrigatório:** não

**Descrição:** palavras-chave relevantes para SEO.

---

### seoRegions

**Tipo:** string

**Obrigatório:** não

**Descrição:** regiões geográficas de atuação.

---

### seoCompetitors

**Tipo:** string

**Obrigatório:** não

**Descrição:** concorrentes considerados para análise de SEO.

---

### analyticsPlatform

**Tipo:** string

**Obrigatório:** não

**Descrição:** ferramenta de analytics utilizada.

---

### campaignPlatforms

**Tipo:** string

**Obrigatório:** não

**Descrição:** plataformas utilizadas em campanhas.

---

# Etapa 13 — Integrações

## Grupo

```text id="e13-group"
integrations
```

---

### needsIntegration

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** indica necessidade de integração com sistemas externos.

---

### systems

**Tipo:** string

**Obrigatório:** não

**Descrição:** sistemas envolvidos na integração.

---

### hasERP

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** necessidade de integração com ERP.

---

### hasCRM

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** necessidade de integração com CRM.

---

### externalApis

**Tipo:** string

**Obrigatório:** não

**Descrição:** APIs externas envolvidas.

---

### importExport

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** necessidade de importação ou exportação de dados.

---

### existingDatabase

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** existência de banco de dados já utilizado pela empresa.

---

### apiDocumentation

**Tipo:** string

**Obrigatório:** não

**Descrição:** documentação disponível para APIs externas.

---

### authenticationMethod

**Tipo:** string

**Obrigatório:** não

**Descrição:** método de autenticação utilizado pelas integrações.

---

### databaseTechnology

**Tipo:** string

**Obrigatório:** não

**Descrição:** tecnologia utilizada no banco de dados existente.

---

# Etapa 14 — Prazo

## Grupo

```text id="e14-group"
timeline
```

---

### estimatedDate

**Tipo:** string

**Obrigatório:** não

**Descrição:** data estimada para entrega.

---

### hasUrgency

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** indica existência de urgência no projeto.

---

### criticalDate

**Tipo:** string

**Obrigatório:** não

**Descrição:** data crítica relacionada ao projeto.

---

### hasProjectStages

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** informa se o projeto será dividido em etapas.

---

### dependencies

**Tipo:** string

**Obrigatório:** não

**Descrição:** dependências internas ou externas.

---

### urgencyReason

**Tipo:** string

**Obrigatório:** não

**Descrição:** motivo da urgência.

---

### projectStages

**Tipo:** string

**Obrigatório:** não

**Descrição:** descrição das etapas previstas.

---

# Etapa 15 — Questões complementares

## Grupo

```text id="e15-group"
additionalQuestions
```

---

### currentProblems

**Tipo:** string

**Obrigatório:** não

**Descrição:** problemas atuais identificados pelo cliente.

---

### currentFailures

**Tipo:** string

**Obrigatório:** não

**Descrição:** processos ou funcionalidades que atualmente não funcionam bem.

---

### limitations

**Tipo:** string

**Obrigatório:** não

**Descrição:** limitações conhecidas.

---

### priorities

**Tipo:** string

**Obrigatório:** não

**Descrição:** pontos considerados prioritários.

---

### futureItems

**Tipo:** string

**Obrigatório:** não

**Descrição:** funcionalidades ou requisitos que podem ficar para versões futuras.

---

# Exemplo da estrutura até a Etapa 15

```json id="e15-example"
{
  "cms": {
    "canEditContent": false,
    "editableContent": "",
    "needsAdminPanel": false,
    "updateResponsible": "",
    "needsTraining": false,
    "autonomyLevel": ""
  },

  "marketing": {
    "needsSEO": false,
    "hasMarketingBlog": false,
    "needsAnalytics": false,
    "usesPixel": false,
    "hasNewsletter": false,
    "campaignIntegration": false
  },

  "integrations": {
    "needsIntegration": false,
    "systems": "",
    "hasERP": false,
    "hasCRM": false,
    "externalApis": ""
  },

  "timeline": {
    "estimatedDate": "",
    "hasUrgency": false,
    "criticalDate": "",
    "hasProjectStages": false
  },

  "additionalQuestions": {
    "currentProblems": "",
    "currentFailures": "",
    "limitations": "",
    "priorities": "",
    "futureItems": ""
  }
}
```
---

# Etapa 16 — Observações finais

## Grupo

```text
finalNotes
```

---

### restrictions

**Tipo:** string

**Obrigatório:** não

**Descrição:** restrições identificadas para o projeto.

---

### extraRequirements

**Tipo:** string

**Obrigatório:** não

**Descrição:** requisitos adicionais informados pelo cliente.

---

### observations

**Tipo:** string

**Obrigatório:** não

**Descrição:** observações gerais relevantes para o projeto.

---

### additionalInformation

**Tipo:** string

**Obrigatório:** não

**Descrição:** informações complementares não contempladas nas etapas anteriores.

---

# Etapa 17 — Processo de aprovação e comunicação

## Grupo

```text
approvalProcess
```

---

### approvalResponsible

**Tipo:** string

**Obrigatório:** não

**Descrição:** responsável principal pelas aprovações.

---

### approvalParticipants

**Tipo:** number

**Obrigatório:** não

**Descrição:** quantidade de pessoas envolvidas no processo de validação.

---

### communicationChannels

**Tipo:** array

**Obrigatório:** não

**Descrição:** canais utilizados para comunicação durante o projeto.

---

### Valores possíveis

```text
email
whatsapp
meetings
platform
other
```

---

### approvalMethod

**Tipo:** string

**Obrigatório:** não

**Descrição:** forma escolhida para aprovação do projeto.

---

### Valores possíveis

```text
beforeDevelopment
byStage
finalVersion
other
```

---

### feedbackDeadline

**Tipo:** string

**Obrigatório:** não

**Descrição:** prazo interno para retorno e aprovação.

---

### thirdPartyApproval

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** existência de aprovações dependentes de terceiros.

---

### communicationNotes

**Tipo:** string

**Obrigatório:** não

**Descrição:** observações relacionadas ao fluxo de comunicação.

---

# Etapa 18 — Pós-lançamento e continuidade

## Grupo

```text
postLaunch
```

---

### postLaunchTraining

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** necessidade de treinamento após a entrega.

---

### desiredAutonomy

**Tipo:** string

**Obrigatório:** não

**Descrição:** nível de autonomia desejado após o lançamento.

---

### supportInterest

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** interesse em suporte contínuo.

---

### futureIntegrations

**Tipo:** boolean

**Obrigatório:** não

**Descrição:** previsão de futuras integrações.

---

### futureExpansion

**Tipo:** string

**Obrigatório:** não

**Descrição:** funcionalidades ou evoluções previstas.

---

### futureExpectations

**Tipo:** string

**Obrigatório:** não

**Descrição:** expectativas de crescimento e evolução do projeto.

---

# Exemplo consolidado de payload

```json
{
  "initialInformation": {},
  "companyInformation": {},
  "projectObjectives": {},
  "targetAudience": {},
  "projectType": {},
  "structure": {},
  "functionalities": {},
  "content": {},
  "design": {},
  "references": {},
  "cms": {},
  "marketing": {},
  "integrations": {},
  "timeline": {},
  "additionalQuestions": {},
  "finalNotes": {},
  "approvalProcess": {},
  "postLaunch": {}
}
```

---

# Checklist de padronização

Antes da implementação recomenda-se verificar:

## Nomenclatura

* [ ] Campos utilizando camelCase.
* [ ] Nomes consistentes em todo o projeto.
* [ ] Sem abreviações desnecessárias.
* [ ] Campos nomeados em inglês.

---

## Tipagem

* [ ] Strings utilizadas para textos.
* [ ] Booleans utilizados para verdadeiro/falso.
* [ ] Arrays utilizados para múltiplas opções.
* [ ] Objects utilizados para agrupamentos.

---

## Estrutura

* [ ] Campos organizados por etapa.
* [ ] Ausência de informações duplicadas.
* [ ] Estrutura preparada para expansão futura.
* [ ] Organização compatível com o formulário.

---

## Qualidade dos dados

* [ ] Campos obrigatórios identificados.
* [ ] Validações previstas.
* [ ] Restrições documentadas.
* [ ] Estrutura revisada antes da implementação.

---

# Benefícios da padronização

A utilização de um schema padronizado traz benefícios como:

* maior consistência dos dados;
* facilidade de manutenção;
* integração simplificada com APIs;
* melhor organização das informações;
* suporte ao processamento automatizado;
* facilidade de evolução futura do projeto.

---

# Considerações finais

Este documento registra uma proposta de organização lógica dos dados coletados pelo formulário de briefing do Portal de Parcerias.

Seu objetivo é servir como referência para nomenclatura, estruturação e padronização das informações coletadas durante o processo de briefing.

A estrutura poderá ser adaptada conforme novas necessidades forem identificadas durante o desenvolvimento do projeto ou durante futuras integrações.

Recomenda-se revisar este documento sempre que houver alterações significativas nas perguntas do formulário ou na forma como os dados são processados.
