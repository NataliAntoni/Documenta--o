# SEO Técnico

## Objetivo

Este documento reúne boas práticas de SEO técnico consideradas durante a fase de estudo e planejamento do Portal de Parcerias da Netz.

As recomendações apresentadas poderão servir como referência para futuras implementações relacionadas ao projeto.

---

## Escopo

Este documento contempla orientações relacionadas a:

* estrutura de páginas;
* conteúdo;
* metadados;
* performance;
* responsividade;
* indexação;
* rastreamento;
* boas práticas de SEO técnico.

---

## Referências

As recomendações presentes neste documento foram baseadas principalmente em:

* Diretrizes do Google Search;
* Google Search Central;
* Lighthouse;
* Core Web Vitals;
* Boas práticas amplamente adotadas em desenvolvimento web.

---

## Conceitos básicos de SEO

### O que é SEO

SEO (Search Engine Optimization) é o conjunto de práticas utilizadas para melhorar a visibilidade de páginas web em mecanismos de busca.

O objetivo é facilitar a compreensão do conteúdo pelos mecanismos de pesquisa e aumentar as chances de que as páginas sejam encontradas pelos usuários.

SEO não depende apenas de conteúdo. Aspectos técnicos, estrutura da página, desempenho e experiência do usuário também influenciam os resultados.

---

### SEO On-Page

SEO On-Page refere-se às otimizações realizadas dentro da própria página.

Exemplos:

* títulos;
* descrições;
* estrutura de conteúdo;
* palavras-chave;
* imagens;
* links internos.

---

### SEO Técnico

SEO Técnico refere-se aos aspectos estruturais e tecnológicos que ajudam mecanismos de busca a rastrear, interpretar e indexar páginas.

Exemplos:

* performance;
* sitemap;
* robots.txt;
* estrutura HTML;
* responsividade;
* acessibilidade.

---

### SEO Off-Page

SEO Off-Page refere-se a fatores externos ao site.

Exemplos:

* backlinks;
* menções da marca;
* compartilhamentos;
* autoridade de domínio.

Embora seja importante, este documento terá foco principal em SEO técnico e SEO On-Page.

---

## Estrutura de páginas

A estrutura da página influencia diretamente a forma como mecanismos de busca interpretam o conteúdo.

Uma estrutura organizada facilita a indexação e melhora a compreensão das informações tanto para usuários quanto para ferramentas de busca.

---

### Título da página (title)

O elemento `title` é um dos fatores mais importantes para SEO On-Page.

Ele define o título exibido:

* nos resultados de busca;
* na aba do navegador;
* em compartilhamentos de links.

Boas práticas:

* possuir um título único para cada página;
* descrever claramente o conteúdo;
* manter títulos objetivos;
* evitar títulos genéricos.

Exemplo recomendado:

```html
<title>Portal de Parcerias | Netz</title>
```

Exemplo a evitar:

```html
<title>Home</title>
```

---

### Meta Description

A meta description é um resumo do conteúdo da página.

Embora não seja um fator direto de ranqueamento, ela influencia a taxa de cliques nos resultados de busca.

Boas práticas:

* descrever o conteúdo da página;
* utilizar linguagem clara;
* evitar descrições duplicadas;
* manter consistência com o conteúdo real da página.

Exemplo:

```html
<meta
  name="description"
  content="Portal de Parcerias da Netz para envio de briefings e gestão de projetos digitais."
/>
```

---

### Hierarquia de títulos

A utilização correta dos títulos ajuda mecanismos de busca a compreenderem a estrutura do conteúdo.

Estrutura recomendada:

* H1 para o título principal;
* H2 para seções;
* H3 para subseções;
* H4 para conteúdos complementares.

Boas práticas:

* utilizar apenas um H1 por página;
* manter hierarquia consistente;
* evitar pular níveis sem necessidade.

Exemplo:

* H1 — Portal de Parcerias

  * H2 — Sobre a Empresa
  * H2 — Funcionalidades

    * H3 — Gestão de Briefings

---

### URLs amigáveis

As URLs devem ser simples, legíveis e descritivas.

Boas práticas:

* utilizar palavras relacionadas ao conteúdo;
* evitar parâmetros desnecessários;
* utilizar hífens para separar palavras;
* manter consistência na estrutura do projeto.

Exemplo recomendado:

```text
/parcerias/novo-briefing
```

Evitar:

```text
/page?id=124&cat=8
```

---

## Conteúdo

O conteúdo continua sendo um dos principais elementos para SEO.

Além de facilitar a indexação, conteúdos bem estruturados contribuem para a experiência do usuário.

---

### Qualidade do conteúdo

O conteúdo deve responder de forma clara às necessidades dos usuários.

Boas práticas:

* fornecer informações úteis;
* evitar textos excessivamente genéricos;
* manter atualização quando necessário;
* priorizar clareza e objetividade.

---

### Palavras-chave

Palavras-chave representam termos que ajudam mecanismos de busca a compreenderem o tema da página.

Boas práticas:

* utilizar palavras-chave naturalmente;
* evitar repetição excessiva;
* distribuir termos relevantes ao longo do conteúdo;
* manter coerência com o objetivo da página.

Evitar práticas conhecidas como "keyword stuffing", caracterizadas pela repetição exagerada de palavras-chave.

---

### Conteúdo duplicado

Conteúdos duplicados podem dificultar a interpretação das páginas pelos mecanismos de busca.

Boas práticas:

* criar conteúdos originais;
* evitar cópias entre páginas;
* manter descrições únicas;
* revisar textos reutilizados.

Quando necessário, utilizar estratégias adequadas para indicar a versão principal de determinado conteúdo.

---

### Organização do conteúdo

Conteúdos extensos devem ser organizados para facilitar leitura e compreensão.

Boas práticas:

* utilizar títulos e subtítulos;
* dividir informações em seções;
* utilizar listas quando apropriado;
* evitar grandes blocos contínuos de texto.

Uma estrutura organizada beneficia tanto usuários quanto mecanismos de busca.

---

## Performance

A performance de uma página influencia diretamente a experiência do usuário e pode impactar a forma como mecanismos de busca avaliam o site.

Páginas lentas tendem a apresentar maiores taxas de abandono, menor engajamento e pior experiência de navegação.

Por esse motivo, a performance deve ser considerada desde o início do desenvolvimento.

---

### Tempo de carregamento

O tempo necessário para exibir o conteúdo da página deve ser reduzido sempre que possível.

Boas práticas:

* minimizar arquivos desnecessários;
* reduzir tamanho de imagens;
* evitar carregamento excessivo de recursos;
* remover dependências não utilizadas;
* utilizar técnicas adequadas de otimização.

O objetivo é entregar o conteúdo principal ao usuário de forma rápida e consistente.

---

### Otimização de imagens

Imagens costumam representar uma parcela significativa do peso total de uma página.

Boas práticas:

* utilizar formatos modernos quando possível;
* redimensionar imagens para o tamanho necessário;
* evitar envio de arquivos excessivamente grandes;
* utilizar compressão adequada;
* remover imagens não utilizadas.

Além de melhorar a performance, essas práticas reduzem o consumo de dados e melhoram a experiência em dispositivos móveis.

---

### Carregamento de recursos

Recursos externos devem ser utilizados com cautela.

Exemplos:

* bibliotecas JavaScript;
* fontes externas;
* vídeos incorporados;
* widgets de terceiros.

Boas práticas:

* carregar apenas o necessário;
* evitar dependências excessivas;
* revisar periodicamente recursos utilizados.

---

### Core Web Vitals

Core Web Vitals são métricas utilizadas pelo Google para avaliar aspectos relacionados à experiência de uso.

Embora os critérios possam evoluir ao longo do tempo, o objetivo permanece o mesmo: medir a qualidade da experiência oferecida ao usuário.

Os principais aspectos avaliados incluem:

* velocidade de carregamento;
* estabilidade visual;
* capacidade de interação.

---

### Estabilidade visual

Elementos da interface não devem mudar de posição inesperadamente durante o carregamento da página.

Problemas comuns:

* imagens sem dimensões definidas;
* carregamento tardio de componentes;
* inserção repentina de conteúdo.

Boas práticas:

* definir dimensões de elementos visuais;
* reservar espaço para conteúdos dinâmicos;
* evitar deslocamentos inesperados da interface.

---

### Interatividade

A interface deve responder adequadamente às ações dos usuários.

Boas práticas:

* reduzir bloqueios causados por scripts;
* evitar excesso de processamento no carregamento inicial;
* garantir que botões e formulários estejam disponíveis rapidamente.

---

## Responsividade

A responsividade é um dos fatores mais importantes para projetos web modernos.

As páginas devem funcionar adequadamente em diferentes tamanhos de tela e dispositivos.

---

### Adaptação para dispositivos móveis

Os conteúdos devem permanecer legíveis e funcionais em smartphones e tablets.

Boas práticas:

* evitar elementos que ultrapassem a largura da tela;
* manter espaçamento adequado;
* utilizar fontes legíveis;
* garantir facilidade de interação por toque.

---

### Mobile First

Sempre que possível, recomenda-se considerar a experiência móvel desde as etapas iniciais do desenvolvimento.

Benefícios:

* melhor adaptação a diferentes dispositivos;
* redução de problemas de layout;
* foco em conteúdos essenciais;
* melhor experiência para usuários móveis.

---

### Navegação em dispositivos móveis

Menus, formulários e componentes devem permanecer utilizáveis em telas menores.

Boas práticas:

* utilizar áreas de toque adequadas;
* evitar elementos excessivamente pequenos;
* manter menus simples e acessíveis;
* reduzir complexidade visual quando necessário.

---

### Compatibilidade entre dispositivos

As páginas devem ser testadas em diferentes resoluções e contextos de uso.

Exemplos:

* smartphones;
* tablets;
* notebooks;
* monitores maiores.

O objetivo é garantir consistência de funcionamento independentemente do dispositivo utilizado.

---

## Relação entre SEO e experiência do usuário

SEO moderno não depende apenas de palavras-chave.

Fatores relacionados à experiência do usuário também influenciam o desempenho das páginas nos mecanismos de busca.

Exemplos:

* velocidade de carregamento;
* acessibilidade;
* responsividade;
* organização do conteúdo;
* facilidade de navegação.

Por esse motivo, recomenda-se que decisões de SEO sejam consideradas em conjunto com práticas de UX e acessibilidade.

---

## Links

Os links ajudam mecanismos de busca a compreender a relação entre páginas e conteúdos.

Além disso, contribuem para a navegação dos usuários e para a descoberta de informações relevantes dentro do projeto.

---

### Links internos

Links internos conectam páginas do mesmo site.

Exemplos:

* página inicial → serviços;
* serviços → contato;
* blog → artigo relacionado.

Boas práticas:

* criar conexões relevantes entre conteúdos;
* facilitar a navegação do usuário;
* utilizar textos descritivos nos links;
* evitar excesso de links desnecessários.

Exemplo recomendado:

* Conheça nossos serviços de desenvolvimento web.

Evitar:

* Clique aqui.

---

### Links externos

Links externos apontam para páginas fora do site.

Podem ser utilizados para:

* referências;
* documentações;
* conteúdos complementares;
* parceiros.

Boas práticas:

* utilizar fontes confiáveis;
* verificar periodicamente se os links continuam válidos;
* garantir que os links possuam contexto adequado.

---

## Indexação

Para que uma página apareça nos resultados de busca, ela precisa ser rastreada e indexada pelos mecanismos de pesquisa.

Uma estrutura técnica adequada facilita esse processo.

Boas práticas:

* disponibilizar páginas importantes para rastreamento;
* evitar bloqueios acidentais;
* manter arquitetura organizada;
* revisar configurações de indexação durante publicações.

---

## Sitemap

O sitemap é um arquivo que informa aos mecanismos de busca quais páginas fazem parte do site.

Seu objetivo é facilitar o rastreamento e descoberta de conteúdos.

Benefícios:

* auxilia mecanismos de busca;
* melhora a descoberta de páginas;
* facilita indexação de conteúdos novos.

Boas práticas:

* manter sitemap atualizado;
* incluir páginas relevantes;
* remover páginas obsoletas quando necessário.

---

## Robots.txt

O arquivo robots.txt informa quais áreas do site podem ou não ser rastreadas por mecanismos de busca.

Exemplos de uso:

* bloquear áreas administrativas;
* evitar indexação de páginas temporárias;
* restringir conteúdos internos.

Importante:

O robots.txt não deve ser utilizado como mecanismo de segurança, pois apenas orienta o comportamento de rastreamento.

---

## Dados estruturados

Dados estruturados ajudam mecanismos de busca a compreender melhor o conteúdo de uma página.

Eles permitem fornecer informações adicionais sobre determinados conteúdos.

Exemplos:

* empresa;
* artigo;
* produto;
* evento;
* FAQ.

Benefícios:

* melhor interpretação do conteúdo;
* possibilidade de recursos avançados nos resultados de busca;
* maior padronização das informações.

---

## SEO para formulários

Embora formulários normalmente não sejam conteúdos destinados ao ranqueamento, algumas boas práticas podem contribuir para melhor compreensão da página.

Boas práticas:

* utilizar títulos claros;
* estruturar corretamente os campos;
* utilizar labels adequadas;
* manter URLs compreensíveis;
* fornecer contexto sobre o objetivo do formulário.

No contexto do Portal de Parcerias, essas práticas auxiliam tanto mecanismos de busca quanto usuários durante o preenchimento do briefing.

---

## SEO para landing pages

Landing pages geralmente possuem objetivos específicos, como geração de leads ou divulgação de serviços.

Boas práticas:

* possuir objetivo claro;
* utilizar título principal descritivo;
* apresentar proposta de valor logo no início da página;
* utilizar chamadas para ação objetivas;
* evitar excesso de informações irrelevantes.

---

## SEO para conteúdo institucional

Projetos institucionais normalmente dependem de clareza e organização das informações.

Boas práticas:

* apresentar claramente a empresa;
* descrever produtos e serviços;
* disponibilizar informações de contato;
* estruturar páginas de forma lógica;
* manter conteúdo atualizado.

---

## Boas práticas de manutenção

SEO não deve ser tratado como uma atividade realizada apenas no lançamento do projeto.

Recomenda-se manutenção periódica para identificar oportunidades de melhoria.

Exemplos:

* atualização de conteúdos;
* revisão de links quebrados;
* análise de desempenho;
* revisão de metadados;
* monitoramento de indexação.

A manutenção contínua contribui para preservar a qualidade técnica do projeto ao longo do tempo.

---

## Checklist de validação

Antes da publicação de uma página ou projeto, recomenda-se verificar os seguintes pontos.

### Estrutura

* [ ] Existe apenas um H1 na página.
* [ ] Os títulos seguem hierarquia lógica.
* [ ] As páginas possuem título (`title`) definido.
* [ ] As páginas possuem meta description configurada.
* [ ] As URLs são amigáveis e descritivas.

---

### Conteúdo

* [ ] O conteúdo é relevante para o objetivo da página.
* [ ] Não existem conteúdos duplicados.
* [ ] As palavras-chave foram utilizadas naturalmente.
* [ ] Os textos estão organizados em seções e subtítulos.
* [ ] O conteúdo está atualizado.

---

### Links

* [ ] Os links internos funcionam corretamente.
* [ ] Os links externos apontam para fontes confiáveis.
* [ ] Não existem links quebrados.
* [ ] Os textos dos links são descritivos.

---

### Imagens

* [ ] As imagens estão otimizadas.
* [ ] Os arquivos possuem tamanho adequado.
* [ ] As imagens relevantes possuem texto alternativo.
* [ ] Não existem imagens desnecessariamente pesadas.

---

### Performance

* [ ] O carregamento da página é adequado.
* [ ] Recursos não utilizados foram removidos.
* [ ] Imagens foram otimizadas.
* [ ] Bibliotecas externas foram revisadas.
* [ ] Não existem recursos bloqueando desnecessariamente o carregamento.

---

### Responsividade

* [ ] A página funciona em dispositivos móveis.
* [ ] O conteúdo permanece legível em diferentes tamanhos de tela.
* [ ] Os elementos interativos possuem tamanho adequado para toque.
* [ ] Não existem problemas de layout em resoluções menores.

---

### Indexação

* [ ] O sitemap está atualizado.
* [ ] O robots.txt está configurado corretamente.
* [ ] As páginas importantes podem ser rastreadas.
* [ ] Não existem bloqueios acidentais de indexação.

---

## Ferramentas recomendadas

As ferramentas abaixo podem auxiliar na análise e validação de aspectos relacionados ao SEO.

### Lighthouse

Ferramenta integrada aos navegadores baseados em Chromium.

Pode auxiliar na análise de:

* SEO;
* acessibilidade;
* performance;
* boas práticas.

---

### Google Search Console

Ferramenta utilizada para monitoramento da presença de páginas nos resultados de busca.

Permite acompanhar:

* indexação;
* cobertura;
* desempenho;
* problemas identificados pelo Google.

---

### PageSpeed Insights

Ferramenta utilizada para avaliação de performance e experiência de usuário.

Auxilia na análise de:

* velocidade de carregamento;
* Core Web Vitals;
* oportunidades de otimização.

---

### Validação manual

Além das ferramentas automatizadas, recomenda-se realizar verificações manuais.

Exemplos:

* revisão de títulos;
* revisão de descrições;
* validação de links;
* revisão de conteúdo;
* testes em dispositivos móveis.

---

## Limitações das ferramentas automáticas

Ferramentas de SEO ajudam a identificar diversos problemas técnicos, mas não substituem análise humana.

Aspectos como qualidade do conteúdo, clareza da comunicação e adequação ao público dependem de avaliação contextual.

Por esse motivo, recomenda-se combinar ferramentas automatizadas e revisão manual.

---

## Relação entre SEO, UX e acessibilidade

SEO, experiência do usuário e acessibilidade possuem objetivos complementares.

Diversas práticas contribuem simultaneamente para essas áreas.

Exemplos:

* estrutura semântica adequada;
* organização do conteúdo;
* responsividade;
* desempenho;
* navegação clara.

A adoção dessas práticas tende a beneficiar usuários e mecanismos de busca.

---

## Considerações finais

Durante a Fase 0 do projeto, o SEO foi considerado como um dos aspectos importantes para garantir qualidade técnica, organização do conteúdo e potencial de descoberta das páginas relacionadas ao Portal de Parcerias.

As recomendações registradas neste documento têm como objetivo servir como referência para futuras implementações e processos de validação.

Este documento não substitui a documentação oficial dos mecanismos de busca, mas reúne práticas consideradas relevantes para o contexto do projeto.

---

## Próximos passos

Para evoluções futuras, recomenda-se:

* aprofundar validações utilizando ferramentas especializadas;
* monitorar desempenho após publicação;
* revisar conteúdos periodicamente;
* acompanhar mudanças em boas práticas de SEO;
* atualizar a documentação quando necessário.

SEO deve ser tratado como um processo contínuo de melhoria e manutenção ao longo do ciclo de vida do projeto.
