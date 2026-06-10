# Accessibility Guidelines

## Objetivo

Este documento reúne as diretrizes de acessibilidade consideradas durante a Fase 0 do projeto da Netz.

Seu objetivo é registrar práticas recomendadas com base na WCAG 2.1 nível AA, servindo como referência para o desenvolvimento do formulário de briefing e demais interfaces previstas durante a Fase 0 do projeto.

A adoção dessas práticas busca promover uma experiência mais inclusiva, acessível e consistente para diferentes perfis de usuários, além de reduzir barreiras de navegação e interação.

---

## Escopo

As recomendações descritas neste documento foram consideradas durante o desenvolvimento da Fase 0 do projeto e devem servir como referência para:

- formulário de briefing;
- Portal de Parcerias;
- interfaces administrativas previstas para a Fase 0;
- componentes reutilizáveis desenvolvidos durante o projeto.

Este documento não substitui a documentação oficial da WCAG, mas consolida diretrizes práticas consideradas relevantes para o contexto do projeto.

---

## Referências

As recomendações apresentadas neste documento foram baseadas principalmente nas seguintes fontes:

- WCAG 2.1 (Web Content Accessibility Guidelines);
- W3C Web Accessibility Initiative (WAI);
- Nielsen Norman Group (NNG);
- boas práticas de UX para formulários;
- boas práticas de desenvolvimento web acessível.

### Links de referência

- https://www.w3.org/WAI/standards-guidelines/wcag/
- https://www.w3.org/WAI/
- https://www.nngroup.com/

---

## O que é acessibilidade?

Acessibilidade digital consiste em desenvolver produtos, serviços e interfaces que possam ser utilizados pelo maior número possível de pessoas, incluindo usuários com limitações visuais, auditivas, motoras, cognitivas ou situacionais.

Aplicar acessibilidade não beneficia apenas pessoas com deficiência. As boas práticas também contribuem para:

- melhorar a experiência de uso;
- aumentar a clareza das interfaces;
- reduzir erros de interação;
- facilitar o uso em dispositivos móveis;
- tornar o conteúdo mais compreensível para diferentes perfis de usuários.

Para este projeto, foi adotada como referência a WCAG 2.1 nível AA, amplamente utilizada como padrão de acessibilidade para aplicações web.

---

## Princípios de acessibilidade

As diretrizes da WCAG são organizadas em quatro princípios fundamentais. Esses princípios servem como base para a construção de interfaces acessíveis e devem ser considerados durante o desenvolvimento do projeto.

### Perceptível

As informações e elementos da interface devem ser apresentados de forma que possam ser percebidos pelos usuários.

Exemplos:

* utilizar contraste adequado entre texto e fundo;
* fornecer texto alternativo para imagens relevantes;
* garantir que informações importantes não dependam exclusivamente de elementos visuais;
* permitir leitura adequada em diferentes tamanhos de tela.

### Operável

Os componentes da interface devem ser utilizáveis por diferentes formas de interação.

Exemplos:

* permitir navegação por teclado;
* disponibilizar foco visível nos elementos interativos;
* evitar interações que dependam exclusivamente do mouse;
* garantir áreas de clique adequadas para botões e links.

### Compreensível

As informações e interações devem ser fáceis de entender.

Exemplos:

* utilizar linguagem clara e objetiva;
* fornecer instruções quando necessário;
* apresentar mensagens de erro compreensíveis;
* manter consistência entre páginas e componentes.

### Robusto

O conteúdo deve funcionar adequadamente em diferentes navegadores, dispositivos e tecnologias assistivas.

Exemplos:

* utilizar HTML semântico;
* respeitar padrões web;
* manter compatibilidade com leitores de tela;
* evitar soluções que dependam exclusivamente de tecnologias específicas.

---

## Estrutura semântica

Sempre que possível, devem ser utilizados elementos HTML semânticos para representar corretamente a estrutura da página.

A utilização adequada desses elementos facilita a navegação por tecnologias assistivas e melhora a compreensão da interface.

### Elementos recomendados

Exemplos de elementos semânticos:

* `<header>`
* `<nav>`
* `<main>`
* `<section>`
* `<article>`
* `<aside>`
* `<footer>`

### Evitar uso excessivo de elementos genéricos

Embora elementos como `div` e `span` sejam úteis, eles não devem substituir elementos semânticos quando existir uma opção mais adequada.

Exemplo recomendado:

* utilizar `<header>` para o cabeçalho;
* utilizar `<nav>` para navegação;
* utilizar `<main>` para conteúdo principal.

Evitar utilizar apenas múltiplas `div`s para representar toda a estrutura da página.

---

## Hierarquia de títulos

Os títulos devem seguir uma ordem lógica e hierárquica.

Uma estrutura adequada auxilia usuários e tecnologias assistivas a compreenderem a organização do conteúdo.

### Exemplo de hierarquia

* H1 — título principal da página;
* H2 — seções principais;
* H3 — subseções;
* H4 — conteúdos complementares.

### Boas práticas

* utilizar apenas um H1 por página;
* manter ordem lógica entre os níveis;
* evitar pular níveis sem necessidade;
* utilizar títulos que descrevam claramente o conteúdo da seção.

### Exemplo recomendado

* H1 — Portal de Parcerias

  * H2 — Informações da Empresa

    * H3 — Dados de Contato
  * H2 — Objetivos do Projeto

### Exemplo a evitar

* H1 — Portal de Parcerias

  * H4 — Dados de Contato
  * H2 — Objetivos do Projeto

Nesse caso, a hierarquia fica inconsistente e pode dificultar a compreensão da estrutura da página por usuários e tecnologias assistivas.

---

## Formulários

Os formulários representam um dos principais pontos de interação entre usuários e sistemas. Durante o desenvolvimento do formulário de briefing, devem ser consideradas práticas que reduzam barreiras de uso e facilitem o preenchimento das informações.

### Labels

Todos os campos devem possuir uma identificação clara e visível.

Boas práticas:

* utilizar labels associadas aos campos;
* posicionar a identificação próxima ao campo correspondente;
* utilizar textos objetivos e de fácil compreensão.

Exemplo recomendado:

* Nome da empresa
* E-mail para contato
* Telefone

Evitar:

* utilizar apenas placeholders como identificação do campo;
* utilizar termos ambíguos ou genéricos.

---

### Campos obrigatórios

Campos obrigatórios devem ser identificados de forma clara.

Boas práticas:

* indicar visualmente quais campos são obrigatórios;
* informar ao usuário quais informações são necessárias para prosseguir;
* manter consistência na identificação dos campos obrigatórios.

Exemplo:

* Nome da empresa *
* E-mail *
* Telefone

Sempre que possível, informar o significado do símbolo utilizado.

Exemplo:

Campo obrigatório (*)

---

### Instruções e ajuda contextual

Quando uma pergunta puder gerar dúvidas, recomenda-se fornecer orientações complementares.

Exemplos:

* descrição breve do objetivo da etapa;
* exemplos de preenchimento;
* explicações sobre informações solicitadas.

O objetivo é reduzir incertezas e evitar respostas incompletas.

---

### Mensagens de erro

Mensagens de erro devem ajudar o usuário a identificar e corrigir o problema encontrado.

Boas práticas:

* explicar claramente o erro;
* indicar como corrigi-lo;
* utilizar linguagem simples e objetiva.

Exemplo recomendado:

* E-mail inválido. Informe um endereço de e-mail válido.

Evitar mensagens genéricas como:

* Erro ao enviar formulário.
* Campo inválido.

---

### Validação de dados

Sempre que possível, recomenda-se validar as informações antes do envio final.

Exemplos:

* formato de e-mail;
* formato de telefone;
* URLs válidas;
* campos obrigatórios preenchidos.

O objetivo é evitar erros que poderiam ser identificados durante o preenchimento.

---

### Ordem de navegação

A navegação por teclado deve seguir uma sequência lógica.

Fluxo esperado:

1. primeiro campo da etapa;
2. segundo campo;
3. terceiro campo;
4. botão de continuar.

A ordem de navegação deve acompanhar a ordem visual apresentada na interface.

---

### Agrupamento de informações

Campos relacionados devem ser organizados em grupos ou seções.

Exemplos:

* informações da empresa;
* objetivos do projeto;
* público-alvo;
* funcionalidades;
* marketing.

Essa organização reduz a carga cognitiva e facilita o preenchimento.

---

### Formulários em múltiplas etapas

Durante os estudos realizados para a Fase 0, identificou-se que formulários divididos em etapas podem reduzir a sobrecarga de informações e melhorar a experiência de preenchimento em processos extensos.

Boas práticas:

* dividir grandes quantidades de informações em etapas menores;
* apresentar apenas informações relevantes para o momento atual;
* permitir avanço e retorno entre etapas;
* informar claramente o progresso do preenchimento.

---

### Barra de progresso

Em formulários extensos, recomenda-se informar visualmente o progresso do usuário.

Benefícios:

* reduz sensação de incerteza;
* ajuda a criar expectativa sobre o restante do processo;
* melhora a percepção de controle durante o preenchimento.

Exemplo:

* Etapa 3 de 18
* 30% concluído

---

### Campos condicionais

Quando aplicável, perguntas adicionais podem ser exibidas com base nas respostas anteriores.
Essa abordagem contribui para a redução da carga cognitiva ao apresentar apenas informações relevantes para cada contexto.

Exemplo:

* Usuário seleciona "E-commerce";
* Sistema exibe perguntas relacionadas a pagamentos e catálogo de produtos.

Benefícios:

* reduz volume de informações exibidas simultaneamente;
* mantém o formulário mais objetivo;
* evita perguntas irrelevantes para determinados projetos.

---

### Revisão antes do envio

Sempre que possível, recomenda-se permitir que o usuário revise as informações antes do envio final.

Benefícios:

* redução de erros;
* maior confiança no processo;
* oportunidade de correção antes da submissão.

---

### Considerações para o formulário de briefing

Durante a definição do formulário de briefing da Fase 0, foram considerados os seguintes princípios:

* organização das perguntas em múltiplas etapas;
* agrupamento lógico das informações;
* validação de dados obrigatórios;
* utilização de linguagem clara;
* possibilidade de utilização futura de campos condicionais;
* sinalização visual do progresso de preenchimento.

Essas decisões foram tomadas com base em estudos de UX para formulários e recomendações de acessibilidade aplicáveis ao contexto do projeto.

---

## Navegação por teclado

Toda funcionalidade importante da interface deve poder ser utilizada sem a necessidade de mouse.

Usuários que utilizam teclado, tecnologias assistivas ou dispositivos alternativos dependem de uma navegação previsível e consistente.

Boas práticas:

* permitir acesso a elementos interativos através da tecla Tab;
* manter ordem lógica de navegação;
* garantir acesso a menus, links, botões e formulários;
* evitar componentes que dependam exclusivamente do clique do mouse.

---

## Foco visível

O usuário deve conseguir identificar claramente qual elemento está selecionado durante a navegação por teclado.

Boas práticas:

* destacar visualmente o elemento em foco;
* utilizar indicadores visíveis e consistentes;
* evitar remover o foco padrão sem substituí-lo por uma alternativa adequada.

Evitar:

* ocultar completamente o foco visual;
* utilizar indicadores de foco difíceis de perceber.

---

## Contraste e cores

As cores devem proporcionar leitura confortável e adequada para diferentes perfis de usuários.

Boas práticas:

* utilizar contraste suficiente entre texto e fundo;
* garantir legibilidade em diferentes dispositivos;
* testar combinações de cores antes da implementação.

Além disso, informações importantes não devem depender exclusivamente de cor.

Exemplo inadequado:

* campo obrigatório identificado apenas pela cor vermelha.

Exemplo recomendado:

* campo obrigatório identificado por cor e símbolo visual;
* mensagens de erro acompanhadas de texto explicativo.

---

## Imagens

Imagens que possuem significado ou transmitem informação relevante devem possuir descrição alternativa.

Boas práticas:

* utilizar texto alternativo quando a imagem possuir conteúdo informativo;
* descrever a finalidade da imagem;
* manter descrições objetivas.

Exemplos:

* logotipo da empresa;
* ícones com função específica;
* gráficos e elementos informativos.

Imagens puramente decorativas podem ser ignoradas por tecnologias assistivas quando apropriado.

---

## Links

Os links devem indicar claramente para onde conduzem o usuário.

Boas práticas:

* utilizar textos descritivos;
* informar claramente o destino ou ação esperada.

Exemplo recomendado:

* Baixar guia de preenchimento do briefing

Evitar:

* Clique aqui
* Saiba mais
* Link

Quando utilizados isoladamente, esses textos fornecem pouco contexto.

---

## Botões

Botões devem representar ações de forma clara e objetiva.

Exemplos:

* Continuar
* Voltar
* Enviar briefing
* Salvar informações

Evitar textos genéricos ou pouco descritivos.

---

## Responsividade

As interfaces devem funcionar adequadamente em diferentes tamanhos de tela e dispositivos.

Boas práticas:

* adaptação para dispositivos móveis;
* redimensionamento adequado dos elementos;
* manutenção da legibilidade dos conteúdos;
* preservação da funcionalidade em diferentes resoluções.

O objetivo é garantir que a experiência permaneça acessível independentemente do dispositivo utilizado.

---

## Conteúdo textual

Os conteúdos apresentados ao usuário devem priorizar clareza e compreensão.

Boas práticas:

* utilizar linguagem simples;
* evitar termos excessivamente técnicos quando não forem necessários;
* dividir informações extensas em blocos menores;
* utilizar títulos e subtítulos para organizar o conteúdo.

Essas recomendações também contribuem para a redução da carga cognitiva durante a navegação.

---

## Mensagens e feedbacks

O sistema deve fornecer retorno claro sobre ações executadas pelo usuário.

Exemplos:

* confirmação de envio;
* mensagens de sucesso;
* mensagens de erro;
* avisos de validação.

O feedback ajuda o usuário a compreender o estado atual da interface e reduz incertezas durante o uso.

---

## Responsabilidade compartilhada

A acessibilidade deve ser considerada durante todas as etapas do projeto.

Isso inclui:

* definição de requisitos;
* estruturação de conteúdo;
* design de interface;
* desenvolvimento;
* validação e testes.

A adoção de práticas acessíveis desde o início tende a reduzir retrabalho e facilitar futuras evoluções do projeto.

---

## Checklist de validação

Antes da entrega de uma interface, recomenda-se verificar os seguintes pontos:

### Estrutura

* [ ] Existe apenas um H1 na página.
* [ ] Os títulos seguem hierarquia lógica.
* [ ] Foram utilizados elementos HTML semânticos sempre que possível.
* [ ] A estrutura da página está organizada de forma clara.

### Formulários

* [ ] Todos os campos possuem identificação visível.
* [ ] Campos obrigatórios estão sinalizados.
* [ ] Mensagens de erro são compreensíveis.
* [ ] A navegação por teclado funciona corretamente.
* [ ] A ordem de navegação acompanha a ordem visual.

### Conteúdo

* [ ] Os textos utilizam linguagem clara e objetiva.
* [ ] Existem instruções quando necessárias.
* [ ] Links possuem descrições adequadas.
* [ ] Botões descrevem corretamente suas ações.

### Visual

* [ ] O contraste entre texto e fundo é adequado.
* [ ] Informações importantes não dependem apenas de cor.
* [ ] O foco visual está visível durante a navegação por teclado.
* [ ] O conteúdo permanece legível em diferentes tamanhos de tela.

### Imagens

* [ ] Imagens informativas possuem descrição adequada.
* [ ] Elementos decorativos não interferem na navegação.

### Responsividade

* [ ] O conteúdo adapta-se corretamente a dispositivos móveis.
* [ ] Não há perda de funcionalidade em telas menores.
* [ ] Os elementos continuam acessíveis em diferentes resoluções.

---

## Ferramentas recomendadas

As seguintes ferramentas podem auxiliar na identificação de problemas de acessibilidade durante o desenvolvimento:

### Lighthouse

Ferramenta integrada aos navegadores baseados em Chromium.

Pode ser utilizada para verificar:

* acessibilidade;
* performance;
* SEO;
* boas práticas.

### WAVE

Ferramenta de análise de acessibilidade desenvolvida pela WebAIM.

Pode auxiliar na identificação de:

* problemas de contraste;
* estrutura de títulos;
* ausência de descrições;
* problemas de navegação.

### Validação manual

Além de ferramentas automatizadas, recomenda-se realizar verificações manuais.

Exemplos:

* navegar utilizando apenas teclado;
* testar formulários completos;
* verificar mensagens de erro;
* validar legibilidade em dispositivos móveis.

---

## Limitações da validação automática

Ferramentas automatizadas auxiliam na identificação de problemas, mas não substituem revisão humana.

Alguns aspectos dependem de avaliação manual, como:

* clareza da linguagem;
* compreensão das instruções;
* qualidade das mensagens de erro;
* organização das informações;
* experiência geral de uso.

Por esse motivo, recomenda-se combinar testes automatizados e validações manuais.

---

## Considerações finais

Durante a Fase 0 do projeto, a acessibilidade foi considerada um dos pilares para a definição da experiência de uso do formulário de briefing e das interfaces previstas para o Portal de Parcerias.

As recomendações registradas neste documento têm como objetivo servir como referência para decisões de design, desenvolvimento e validação, contribuindo para uma experiência mais inclusiva e consistente.

Este documento não pretende substituir a documentação oficial da WCAG, mas consolidar os principais pontos considerados relevantes para o contexto do projeto.

---

## Próximos passos

Para evoluções futuras do projeto, recomenda-se:

* aprofundar testes de acessibilidade durante o desenvolvimento;
* validar componentes reutilizáveis sob a perspectiva da WCAG;
* incorporar critérios de acessibilidade aos processos de revisão;
* realizar testes com usuários sempre que possível;
* manter a documentação atualizada conforme novas necessidades surgirem.

A acessibilidade deve ser tratada como um processo contínuo de melhoria, e não apenas como uma etapa final de validação.


