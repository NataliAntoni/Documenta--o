# Componentes do Formulário de Briefing

## Objetivo

Este documento registra os principais componentes de interface identificados durante o desenvolvimento do fluxo de briefing do Portal de Parcerias.

Seu objetivo é documentar a função, utilização e boas práticas associadas aos elementos que compõem a experiência de preenchimento do formulário.

---

## Escopo

Este documento não define uma biblioteca oficial de componentes da empresa.

Seu foco está exclusivamente nos componentes previstos para o formulário de briefing estudado durante a Fase 0 do Portal de Parcerias.

---

## Visão geral dos componentes

Os componentes documentados neste arquivo foram identificados a partir do wireframe textual e da estrutura definida para o formulário.

Principais componentes:

* Header
* Barra de progresso
* Container de etapa
* Campos de formulário
* Mensagens de validação
* Navegação entre etapas
* Tela de confirmação

Cada componente possui uma função específica dentro da experiência de preenchimento do briefing.

---

## Princípios gerais

Todos os componentes devem seguir os princípios definidos nos documentos de acessibilidade e usabilidade.

Recomenda-se:

* linguagem clara;
* identificação adequada dos campos;
* consistência visual;
* feedback ao usuário;
* acessibilidade por teclado;
* compatibilidade com leitores de tela.

---

# Header

## Objetivo

O Header tem a função de identificar o sistema e contextualizar o usuário durante o preenchimento do briefing.

---

## Conteúdo previsto

O componente poderá conter:

* logotipo da Netz;
* nome do sistema;
* identificação da etapa atual.

---

## Boas práticas

* manter estrutura simples;
* evitar excesso de informações;
* garantir boa legibilidade;
* manter consistência visual entre etapas.

---

## Considerações de acessibilidade

* utilizar elementos semânticos apropriados;
* manter contraste adequado;
* evitar informações transmitidas apenas por elementos visuais.

---

# Barra de progresso

## Objetivo

A barra de progresso informa ao usuário sua posição dentro do fluxo de preenchimento.

Seu uso busca reduzir incertezas e melhorar a percepção de avanço durante o processo.

---

## Informações apresentadas

Exemplos:

* etapa atual;
* quantidade total de etapas;
* percentual de progresso.

---

## Benefícios

* aumenta previsibilidade;
* reduz sensação de formulário extenso;
* melhora orientação do usuário.

---

## Boas práticas

* exibir progresso de forma clara;
* manter atualização consistente;
* evitar informações conflitantes.

---

## Considerações de acessibilidade

* não depender apenas de cores;
* disponibilizar indicação textual da etapa atual;
* garantir leitura adequada por tecnologias assistivas.

---

# Container de etapa

## Objetivo

O Container de Etapa é o componente responsável por agrupar todo o conteúdo relacionado a uma etapa específica do formulário.

Ele organiza visualmente as informações e auxilia o usuário a compreender o contexto das perguntas apresentadas.

---

## Conteúdo previsto

Cada container de etapa poderá conter:

* título da etapa;
* descrição da etapa;
* campos de formulário;
* mensagens auxiliares;
* botões de navegação.

---

## Benefícios

* melhora organização visual;
* reduz sobrecarga cognitiva;
* facilita compreensão da estrutura do formulário;
* aumenta consistência entre etapas.

---

## Boas práticas

* manter espaçamento adequado;
* agrupar informações relacionadas;
* evitar excesso de conteúdo em uma única tela;
* manter padrão visual consistente.

---

## Considerações de acessibilidade

* utilizar estrutura semântica adequada;
* manter hierarquia correta de títulos;
* garantir leitura lógica do conteúdo.

---

# Título da etapa

## Objetivo

O título da etapa informa ao usuário qual assunto está sendo tratado naquele momento do preenchimento.

Ele funciona como referência principal para contextualização da etapa atual.

---

## Exemplos

* Informações iniciais
* Sobre a empresa
* Objetivo do projeto
* Público-alvo
* Funcionalidades
* Conteúdo
* Marketing

---

## Benefícios

* melhora orientação do usuário;
* reduz dúvidas durante o preenchimento;
* facilita navegação entre etapas.

---

## Boas práticas

* utilizar textos curtos;
* utilizar linguagem simples;
* manter consistência entre etapas;
* representar claramente o conteúdo apresentado.

---

## Considerações de acessibilidade

* utilizar títulos semânticos;
* respeitar hierarquia de cabeçalhos;
* evitar títulos genéricos ou ambíguos.

---

# Descrição da etapa

## Objetivo

A descrição da etapa apresenta uma breve explicação sobre o propósito das perguntas exibidas.

Seu papel é orientar o usuário antes do preenchimento dos campos.

---

## Exemplo

"Identificar empresa, responsável e contexto básico do projeto."

---

## Benefícios

* reduz incertezas;
* melhora compreensão das perguntas;
* auxilia usuários menos familiarizados com o processo.

---

## Boas práticas

* utilizar linguagem objetiva;
* evitar textos longos;
* explicar claramente o objetivo da etapa.

---

## Considerações de acessibilidade

* manter boa legibilidade;
* utilizar linguagem simples;
* evitar termos excessivamente técnicos.

---

# Grupo de campos

## Objetivo

O Grupo de Campos organiza perguntas relacionadas dentro de uma mesma etapa.

Esse agrupamento facilita a leitura e reduz a sensação de complexidade do formulário.

---

## Exemplos

Grupo de contato:

* nome;
* e-mail;
* telefone.

Grupo de identidade visual:

* logotipo;
* cores;
* fontes.

Grupo de integrações:

* APIs;
* CRM;
* ERP.

---

## Benefícios

* melhora organização;
* facilita preenchimento;
* reduz esforço cognitivo;
* melhora compreensão das informações.

---

## Boas práticas

* agrupar campos relacionados;
* evitar grupos excessivamente grandes;
* manter espaçamento consistente;
* respeitar sequência lógica das perguntas.

---

## Considerações de acessibilidade

* utilizar agrupamentos semânticos quando apropriado;
* fornecer contexto claro para cada conjunto de campos;
* garantir navegação lógica por teclado.

---

# Campos obrigatórios

## Objetivo

Os campos obrigatórios representam informações essenciais para o entendimento do projeto.

Seu preenchimento é necessário para continuidade do fluxo.

---

## Exemplos

* nome da empresa;
* responsável;
* e-mail;
* objetivo principal do projeto.

---

## Boas práticas

* indicar claramente quais campos são obrigatórios;
* evitar quantidade excessiva de obrigatoriedades;
* solicitar apenas informações realmente necessárias.

---

## Considerações de acessibilidade

* não utilizar apenas cor para indicar obrigatoriedade;
* fornecer indicação textual adequada;
* garantir comunicação clara para leitores de tela.

---

# Campos opcionais

## Objetivo

Os campos opcionais permitem coletar informações complementares sem bloquear o avanço do usuário.

---

## Benefícios

* reduz abandono;
* diminui esforço de preenchimento;
* permite aprofundamento quando necessário.

---

## Boas práticas

* identificar claramente como opcional;
* evitar excesso de perguntas opcionais;
* priorizar relevância das informações coletadas.

---

## Considerações de acessibilidade

* comunicar claramente que o preenchimento não é obrigatório;
* manter comportamento consistente com os demais campos.

---

# Campo de texto

## Objetivo

O Campo de Texto é utilizado para coletar informações curtas fornecidas pelo usuário.

É um dos componentes mais utilizados ao longo do formulário.

---

## Exemplos de uso

* nome da empresa;
* nome do projeto;
* nome do responsável;
* cidade;
* segmento de atuação;
* concorrentes.

---

## Benefícios

* preenchimento rápido;
* baixa complexidade;
* adequado para respostas objetivas.

---

## Boas práticas

* utilizar rótulos (labels) claros;
* evitar solicitar múltiplas informações em um único campo;
* fornecer exemplos quando necessário;
* limitar tamanho da resposta quando apropriado.

---

## Considerações de acessibilidade

* associar corretamente label e input;
* manter contraste adequado;
* permitir navegação por teclado;
* exibir mensagens de erro compreensíveis.

---

# Área de texto (Textarea)

## Objetivo

A Área de Texto é utilizada para respostas mais detalhadas e descritivas.

Permite que o usuário forneça informações mais completas sobre o projeto.

---

## Exemplos de uso

* descrição da empresa;
* objetivo do projeto;
* necessidades do público;
* observações finais;
* restrições;
* requisitos extras.

---

## Benefícios

* permite contextualização;
* reduz limitações de resposta;
* facilita coleta de requisitos.

---

## Boas práticas

* utilizar perguntas objetivas;
* evitar textos excessivamente longos;
* orientar o usuário sobre o tipo de informação esperada.

---

## Considerações de acessibilidade

* manter identificação clara;
* permitir redimensionamento quando aplicável;
* garantir compatibilidade com leitores de tela.

---

# Campo de seleção (Select)

## Objetivo

O componente Select permite ao usuário escolher uma opção dentro de uma lista previamente definida.

É recomendado quando existe apenas uma resposta válida entre várias opções.

---

## Exemplos de uso

* tipo de público;
* faixa etária;
* nível de autonomia;
* tipo de suporte.

---

## Benefícios

* reduz erros de preenchimento;
* padroniza respostas;
* facilita processamento posterior dos dados.

---

## Boas práticas

* utilizar opções objetivas;
* evitar listas excessivamente longas;
* organizar opções de forma lógica.

---

## Considerações de acessibilidade

* garantir navegação por teclado;
* manter identificação adequada;
* informar claramente a opção selecionada.

---

# Grupo de checkboxes

## Objetivo

Os Checkboxes permitem selecionar múltiplas opções simultaneamente.

São utilizados quando mais de uma resposta pode ser válida.

---

## Exemplos de uso

Finalidades do projeto:

* captar leads;
* vender;
* divulgar marca;
* automatizar processos.

Funcionalidades:

* login;
* upload;
* painel administrativo;
* notificações.

---

## Benefícios

* permite múltiplas escolhas;
* facilita levantamento de requisitos;
* melhora flexibilidade do formulário.

---

## Boas práticas

* agrupar opções relacionadas;
* utilizar descrições claras;
* evitar excesso de opções em um único grupo.

---

## Considerações de acessibilidade

* associar corretamente labels;
* permitir seleção por teclado;
* manter área clicável adequada.

---

# Grupo de radio buttons

## Objetivo

Os Radio Buttons permitem selecionar apenas uma opção dentro de um conjunto.

São indicados quando as opções são mutuamente exclusivas.

---

## Exemplos de uso

Tipo principal de projeto:

* site institucional;
* portfólio;
* landing page;
* e-commerce;
* sistema interno.

---

## Benefícios

* facilita tomada de decisão;
* reduz ambiguidades;
* melhora padronização dos dados.

---

## Boas práticas

* apresentar todas as opções visíveis;
* utilizar descrições claras;
* evitar quantidade excessiva de alternativas.

---

## Considerações de acessibilidade

* agrupar opções relacionadas;
* permitir navegação por teclado;
* informar claramente qual opção está selecionada.

---

# Campo de URL

## Objetivo

Permitir o envio de links relacionados ao projeto.

---

## Exemplos de uso

* site atual;
* referências;
* concorrentes;
* redes sociais.

---

## Benefícios

* facilita análise de referências;
* centraliza materiais relevantes;
* melhora entendimento do contexto do projeto.

---

## Boas práticas

* validar formato da URL;
* permitir links completos;
* informar exemplos de preenchimento.

---

## Considerações de acessibilidade

* fornecer mensagens de erro claras;
* indicar formato esperado;
* evitar dependência exclusiva de validações visuais.

---

# Campo de e-mail

## Objetivo

Coletar o endereço de e-mail do responsável pelo projeto.

---

## Benefícios

* facilita comunicação;
* reduz erros através de validação específica.

---

## Boas práticas

* utilizar validação adequada;
* informar erros de preenchimento;
* evitar bloqueios desnecessários.

---

## Considerações de acessibilidade

* comunicar erros de forma textual;
* permitir correção simples;
* garantir compatibilidade com tecnologias assistivas.

---

# Campo de telefone

## Objetivo

Coletar informações de contato para comunicação durante o projeto.

---

## Benefícios

* facilita alinhamentos;
* oferece canal alternativo de contato.

---

## Boas práticas

* aceitar formatos comuns;
* orientar preenchimento;
* validar estrutura básica do número.

---

## Considerações de acessibilidade

* fornecer instruções claras;
* não depender exclusivamente de máscaras visuais;
* exibir mensagens de validação compreensíveis.

---

# Mensagens de ajuda

## Objetivo

As Mensagens de Ajuda têm a função de orientar o usuário durante o preenchimento dos campos.

Elas fornecem contexto adicional e auxiliam na compreensão das informações esperadas.

---

## Exemplos de uso

* explicação sobre o objetivo da pergunta;
* exemplos de resposta;
* instruções de preenchimento;
* observações complementares.

---

## Benefícios

* reduz dúvidas;
* melhora qualidade das respostas;
* diminui erros de preenchimento.

---

## Boas práticas

* utilizar linguagem simples;
* manter textos curtos;
* apresentar apenas informações relevantes;
* evitar excesso de instruções.

---

## Considerações de acessibilidade

* garantir boa legibilidade;
* manter contraste adequado;
* associar a mensagem ao campo correspondente quando necessário.

---

# Mensagens de validação

## Objetivo

As Mensagens de Validação informam ao usuário que uma informação foi preenchida corretamente.

Seu papel é fornecer feedback durante o preenchimento do formulário.

---

## Exemplos

* e-mail válido;
* URL válida;
* campo preenchido corretamente.

---

## Benefícios

* aumenta confiança do usuário;
* reduz incertezas;
* melhora experiência de preenchimento.

---

## Boas práticas

* apresentar feedback imediato quando apropriado;
* utilizar mensagens claras;
* evitar excesso de notificações.

---

## Considerações de acessibilidade

* disponibilizar feedback textual;
* não depender apenas de cores ou ícones;
* garantir leitura por tecnologias assistivas.

---

# Mensagens de erro

## Objetivo

As Mensagens de Erro informam que uma ação não pôde ser concluída ou que um campo contém informações inválidas.

---

## Exemplos

* campo obrigatório não preenchido;
* formato de e-mail inválido;
* URL inválida;
* valor incompatível com o formato esperado.

---

## Benefícios

* facilita correção dos problemas;
* reduz frustração;
* melhora qualidade dos dados coletados.

---

## Boas práticas

* informar claramente o problema;
* indicar como corrigi-lo;
* exibir mensagens próximas ao campo afetado;
* evitar mensagens genéricas.

---

## Exemplos de mensagens

Correto:

* "Informe um endereço de e-mail válido."
* "Este campo é obrigatório."

Evitar:

* "Erro."
* "Campo inválido."

---

## Considerações de acessibilidade

* utilizar mensagens textuais;
* permitir identificação fácil do campo com problema;
* garantir leitura por leitores de tela.

---

# Campos condicionais

## Objetivo

Os Campos Condicionais permitem exibir perguntas adicionais com base nas respostas fornecidas anteriormente.

Esse comportamento reduz a quantidade de informações apresentadas simultaneamente.

---

## Exemplos de uso

Pergunta:

"Existe integração com APIs externas?"

Resposta:

"Sim"

Campos exibidos:

* Nome da API;
* Documentação disponível;
* Método de autenticação.

---

## Benefícios

* reduz sobrecarga visual;
* melhora organização do formulário;
* apresenta apenas informações relevantes.

---

## Boas práticas

* exibir campos somente quando necessários;
* manter transições previsíveis;
* evitar mudanças inesperadas na interface.

---

## Considerações de acessibilidade

* informar adequadamente quando novos campos forem exibidos;
* manter ordem lógica de navegação;
* garantir acesso por teclado.

---

# Upload de arquivos

## Objetivo

Permitir o envio de documentos e materiais complementares relacionados ao projeto.

---

## Exemplos de uso

* logotipo;
* manual da marca;
* mapa do site;
* documentos de referência;
* materiais institucionais.

---

## Benefícios

* centraliza informações;
* reduz trocas adicionais de arquivos;
* facilita análise do projeto.

---

## Boas práticas

* informar formatos aceitos;
* informar tamanho máximo permitido;
* indicar claramente quando o envio for concluído.

---

## Considerações de acessibilidade

* permitir seleção por teclado;
* fornecer mensagens claras de sucesso ou erro;
* identificar corretamente o componente para leitores de tela.

---

# Seções expansíveis

## Objetivo

As Seções Expansíveis permitem revelar informações complementares sem aumentar excessivamente o tamanho visual da página.

---

## Possíveis aplicações

* detalhes adicionais;
* explicações técnicas;
* informações opcionais;
* orientações de preenchimento.

---

## Benefícios

* reduz poluição visual;
* melhora organização;
* mantém foco nas informações principais.

---

## Boas práticas

* utilizar títulos claros;
* indicar visualmente o estado expandido ou recolhido;
* evitar ocultar informações essenciais.

---

## Considerações de acessibilidade

* informar corretamente o estado da seção;
* permitir navegação por teclado;
* garantir compatibilidade com leitores de tela.

---

# Feedback de carregamento

## Objetivo

Informar ao usuário que uma ação está em andamento.

---

## Exemplos

* envio do formulário;
* carregamento de dados;
* processamento de arquivos.

---

## Benefícios

* reduz incerteza;
* melhora percepção de desempenho;
* evita ações repetidas.

---

## Boas práticas

* indicar claramente que o sistema está processando uma ação;
* evitar períodos prolongados sem feedback;
* informar conclusão quando possível.

---

## Considerações de acessibilidade

* fornecer mensagens textuais;
* não depender exclusivamente de animações;
* manter compatibilidade com tecnologias assistivas.

---

# Navegação entre etapas

## Objetivo

Os componentes de navegação permitem que o usuário avance ou retorne entre as etapas do formulário de briefing.

Eles são responsáveis por conduzir o fluxo de preenchimento de forma organizada e previsível.

---

## Componentes previstos

* Botão Voltar
* Botão Continuar
* Botão Finalizar

---

## Benefícios

* facilita navegação;
* melhora controle do usuário sobre o processo;
* reduz sensação de bloqueio durante o preenchimento.

---

## Boas práticas

* manter posicionamento consistente;
* utilizar rótulos claros;
* indicar quando uma ação não está disponível;
* evitar mudanças inesperadas de comportamento.

---

## Considerações de acessibilidade

* permitir navegação por teclado;
* manter foco visível;
* utilizar textos compreensíveis;
* garantir área de clique adequada.

---

# Botão Voltar

## Objetivo

Permitir retorno para etapas anteriores sem perda das informações já preenchidas.

---

## Benefícios

* facilita revisão de respostas;
* reduz necessidade de reiniciar o formulário;
* aumenta confiança durante o preenchimento.

---

## Boas práticas

* manter comportamento previsível;
* preservar informações preenchidas;
* indicar claramente sua função.

---

# Botão Continuar

## Objetivo

Permitir avanço para a próxima etapa do formulário.

---

## Benefícios

* orienta o fluxo;
* reforça a progressão do processo;
* melhora organização da experiência.

---

## Boas práticas

* validar campos obrigatórios antes do avanço;
* manter posicionamento consistente;
* fornecer feedback quando houver bloqueios.

---

# Botão Finalizar

## Objetivo

Concluir o processo de preenchimento e realizar o envio das informações.

---

## Benefícios

* encerra o fluxo de forma clara;
* indica conclusão da tarefa;
* prepara o usuário para a próxima etapa do processo.

---

## Boas práticas

* exibir apenas na etapa final;
* solicitar confirmação apenas quando necessário;
* informar resultado do envio.

---

# Tela de confirmação

## Objetivo

Informar ao usuário que o briefing foi enviado com sucesso.

Essa etapa representa o encerramento da interação principal do formulário.

---

## Informações previstas

* mensagem de sucesso;
* confirmação do envio;
* orientações sobre próximos passos;
* prazo estimado de retorno (quando aplicável).

---

## Benefícios

* reduz incertezas;
* confirma conclusão do processo;
* melhora experiência pós-envio.

---

## Boas práticas

* utilizar linguagem clara;
* destacar confirmação de envio;
* informar próximos passos de forma objetiva.

---

## Considerações de acessibilidade

* garantir leitura adequada da mensagem;
* disponibilizar confirmação textual;
* manter estrutura semântica apropriada.

---

# Resumo dos componentes identificados

Os seguintes componentes foram identificados durante a definição do fluxo do formulário de briefing:

### Estrutura

* Header
* Barra de progresso
* Container de etapa
* Título da etapa
* Descrição da etapa
* Grupo de campos

---

### Entrada de dados

* Campo de texto
* Área de texto (Textarea)
* Select
* Checkbox
* Radio Button
* Campo de e-mail
* Campo de telefone
* Campo de URL

---

### Interação e feedback

* Mensagens de ajuda
* Mensagens de validação
* Mensagens de erro
* Campos condicionais
* Upload de arquivos
* Seções expansíveis
* Feedback de carregamento

---

### Navegação

* Botão Voltar
* Botão Continuar
* Botão Finalizar

---

### Encerramento

* Tela de confirmação

---

# Checklist de componentes

Antes da implementação, recomenda-se verificar:

## Estrutura

* [ ] Header definido.
* [ ] Barra de progresso definida.
* [ ] Estrutura de etapas organizada.
* [ ] Hierarquia de títulos validada.

---

## Campos

* [ ] Labels definidos.
* [ ] Campos obrigatórios identificados.
* [ ] Campos opcionais identificados.
* [ ] Validações previstas.

---

## Feedback

* [ ] Mensagens de erro definidas.
* [ ] Mensagens de ajuda definidas.
* [ ] Feedback de carregamento previsto.
* [ ] Mensagem de confirmação definida.

---

## Acessibilidade

* [ ] Navegação por teclado considerada.
* [ ] Hierarquia semântica definida.
* [ ] Contraste adequado.
* [ ] Mensagens compreensíveis para tecnologias assistivas.

---

# Considerações finais

Este documento registra os principais componentes identificados durante a definição do formulário de briefing do Portal de Parcerias.

Seu objetivo é servir como referência para organização da interface, padronização dos elementos utilizados e alinhamento entre as etapas de planejamento e implementação.

Os componentes descritos poderão evoluir conforme novas necessidades forem identificadas durante o desenvolvimento do projeto.

A documentação deve ser revisada sempre que novos componentes forem adicionados ou quando alterações significativas forem realizadas na estrutura do formulário.
