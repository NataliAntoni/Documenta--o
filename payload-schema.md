# payload-schema.md

# Payload Schema - Portal de Parcerias Netz

## Versão

1.0

---

## Objetivo

Este documento define o padrão de estrutura de dados utilizado no Portal de Parcerias Netz para:

- Comunicação entre frontend e backend
- Interpretação dos briefings pela I
- Integração com sistemas externos
- Garantia de consistência dos dados

---

## Convenções de Nomenclatura

| Tipo | Padrão | Exemplo |
| --- | --- | --- |
| Campos | snake_case | `nome_projeto` |
| Arrays | plural | `respostas` |
| Objetos | singular | `cliente` |
| Constantes | UPPER_SNAKE | `STATUS_CHOICES` |
| Códigos de perguntas | snake_case | `nome_empresa` |

---

## Tipos de Dados

| Tipo | Descrição | Exemplo |
| --- | --- | --- |
| string | Texto | `"Cafeteria do João"` |
| number | Número inteiro ou decimal | `15000` |
| boolean | Verdadeiro ou falso | `true` |
| datetime | Data e hora ISO 8601 | `2025-06-15T10:30:00Z` |
| array | Lista de valores | `["pix", "cartao"]` |
| object | Objeto aninhado | `{"nome": "João"}` |
| null | Valor vazio | `null` |

---

## Estrutura Principal do Projeto

### Projeto (modelo principal)

| Campo | Tipo | Obrigatório | Descrição |
| --- | --- | --- | --- |
| `id` | number | Sim | Identificador único do projeto |
| `nome_projeto` | string | Sim | Nome do projeto |
| `tipo_projeto` | string | Sim | Tipo do projeto (ver lista de tipos) |
| `status` | string | Sim | Status atual do briefing |
| `agencia` | object | Não | Dados da agência parceira |
| `cliente` | object | Não | Dados do cliente final |
| `prazo_dias` | number | Não | Prazo estimado em dias |
| `orcamento_sugerido` | number | Não | Orçamento sugerido |
| `orcamento_fechado` | number | Não | Orçamento aprovado |
| `data_criacao` | datetime | Sim | Data de criação do projeto |
| `ultima_atualizacao` | datetime | Sim | Data da última alteração |
| `responsavel_netz` | string | Não | Responsável pelo projeto na Netz |
| `briefing_json` | object | Sim | Todas as respostas do briefing |
| `ordem_personalizada` | array | Não | Ordem das perguntas definida pela IA |
| `sugestoes_respostas` | object | Não | Sugestões de resposta da IA |

---

### Tipos de Projeto (tipo_projeto)

Valores permitidos:

| Valor | Exibição |
| --- | --- |
| `institucional` | Site Institucional |
| `portfolio` | Portfólio |
| `landing_page` | Landing Page |
| `portal` | Portal |
| `dashboard` | Dashboard |
| `sistema_interno` | Sistema Interno |
| `plataforma` | Plataforma |
| `blog` | Blog |
| `ecommerce` | E-commerce |
| `outro` | Outro |

---

### Status do Projeto (status)

| Valor | Exibição | Descrição |
| --- | --- | --- |
| `em_briefing` | Em Briefing | Coletando informações |
| `orcamento_gerado` | Orçamento Gerado | Proposta criada |
| `aprovado` | Aprovado | Proposta aceita |
| `em_execucao` | Em Execução | Projeto em desenvolvimento |
| `concluido` | Concluído | Projeto finalizado |
| `cancelado` | Cancelado | Projeto cancelado |

---

## Estrutura do Briefing (briefing_json)

### Objeto Principal

```json
{
  "projeto_id": 123,
  "data_inicio": "2025-06-15T10:30:00Z",
  "versao_briefing": 1,
  "respostas": {
    "codigo_pergunta_1": "resposta",
    "codigo_pergunta_2": ["opcao1", "opcao2"]
  }
}
```

markdown

```
# Payload Schema - Portal de Parcerias Netz

## Versão

1.0

---

## Objetivo

Este documento define o padrão de estrutura de dados utilizado no Portal de Parcerias Netz para:

* Comunicação entre frontend e backend
* Interpretação dos briefings pela IA
* Integração com sistemas externos
* Garantia de consistência dos dados

---

## Convenções de Nomenclatura

| Tipo| Padrão| Exemplo|
|------|--------|---------|
| Campos| snake_case| `nome_projeto`|
| Arrays| plural| `respostas`|
| Objetos| singular| `cliente`|
| Constantes| UPPER_SNAKE| `STATUS_CHOICES`|
| Códigos de perguntas| snake_case| `nome_empresa`|

---

## Tipos de Dados

| Tipo| Descrição| Exemplo|
|------|-----------|---------|
| string| Texto| `"Cafeteria do João"`|
| number| Número inteiro ou decimal| `15000`|
| boolean| Verdadeiro ou falso| `true`|
| datetime| Data e hora ISO 8601| `2025-06-15T10:30:00Z`|
| array| Lista de valores| `["pix", "cartao"]`|
| object| Objeto aninhado| `{"nome": "João"}`|
| null| Valor vazio| `null`|

---

## Estrutura Principal do Projeto

### Projeto (modelo principal)

| Campo| Tipo| Obrigatório| Descrição|
|-------|------|-------------|-----------|
| `id`| number| Sim| Identificador único do projeto|
| `nome_projeto`| string| Sim| Nome do projeto|
| `tipo_projeto`| string| Sim| Tipo do projeto (ver lista de tipos)|
| `status`| string| Sim| Status atual do briefing|
| `agencia`| object| Não| Dados da agência parceira|
| `cliente`| object| Não| Dados do cliente final|
| `prazo_dias`| number| Não| Prazo estimado em dias|
| `orcamento_sugerido`| number| Não| Orçamento sugerido|
| `orcamento_fechado`| number| Não| Orçamento aprovado|
| `data_criacao`| datetime| Sim| Data de criação do projeto|
| `ultima_atualizacao`| datetime| Sim| Data da última alteração|
| `responsavel_netz`| string| Não| Responsável pelo projeto na Netz|
| `briefing_json`| object| Sim| Todas as respostas do briefing|
| `ordem_personalizada`| array| Não| Ordem das perguntas definida pela IA|
| `sugestoes_respostas`| object| Não| Sugestões de resposta da IA|

---

### Tipos de Projeto (tipo_projeto)

Valores permitidos:

| Valor| Exibição|
|-------|----------|
| `institucional`| Site Institucional|
| `portfolio`| Portfólio|
| `landing_page`| Landing Page|
| `portal`| Portal|
| `dashboard`| Dashboard|
| `sistema_interno`| Sistema Interno|
| `plataforma`| Plataforma|
| `blog`| Blog|
| `ecommerce`| E-commerce|
| `outro`| Outro|

---

### Status do Projeto (status)

| Valor| Exibição| Descrição|
|-------|----------|-----------|
| `em_briefing`| Em Briefing| Coletando informações|
| `orcamento_gerado`| Orçamento Gerado| Proposta criada|
| `aprovado`| Aprovado| Proposta aceita|
| `em_execucao`| Em Execução| Projeto em desenvolvimento|
| `concluido`| Concluído| Projeto finalizado|
| `cancelado`| Cancelado| Projeto cancelado|

---

## Estrutura do Briefing (briefing_json)

### Objeto Principal

```json
{
  "projeto_id": 123,
  "data_inicio": "2025-06-15T10:30:00Z",
  "versao_briefing": 1,
  "respostas": {
    "codigo_pergunta_1": "resposta",
    "codigo_pergunta_2": ["opcao1", "opcao2"]
  }
}
```

### **Campos do Objeto**

| **Campo** | **Tipo** | **Obrigatório** | **Descrição** |
| --- | --- | --- | --- |
| `projeto_id` | number | Sim | ID do projeto no sistema |
| `data_inicio` | datetime | Sim | Data de início do briefing |
| `versao_briefing` | number | Sim | Versão do schema (incrementar em mudanças) |
| `respostas` | object | Sim | Dicionário de respostas (código → valor) |

---

## **Códigos de Perguntas (snake_case)**

### **Grupo 1 - Empresa**

| **Código** | **Tipo** | **Obrigatório** |
| --- | --- | --- |
| `nome_empresa` | string | Sim |
| `nome_projeto` | string | Sim |
| `responsavel` | string | Sim |
| `email` | email | Sim |
| `telefone` | string | Não |
| `site_atual` | url | Não |
| `redes_sociais` | string | Não |
| `segmento` | string | Sim |
| `cidade_pais` | string | Não |
| `o_que_faz` | string | Não |
| `produtos_servicos` | string | Não |

### **Grupo 2 - Projeto**

| **Código** | **Tipo** | **Obrigatório** |
| --- | --- | --- |
| `principal_objetivo` | string | Sim |
| `problema_resolve` | string | Não |
| `espera_alcancar` | string | Não |
| `finalidade` | array | Não |
| `publico_principal` | string | Sim |
| `b2b_b2c` | string | Não |
| `faixa_etaria` | string | Não |
| `tipo_projeto` | string | Sim |

### **Grupo 3 - Funcionalidades**

| **Código** | **Tipo** | **Obrigatório** |
| --- | --- | --- |
| `paginas_necessarias` | string | Não |
| `acao_principal` | string | Não |
| `funcionalidades` | array | Não |
| `area_restrita` | boolean | Não |
| `precisa_integracao` | boolean | Não |
| `quais_sistemas` | string | Não |

### **Grupo 4 - Conteúdo e Design**

| **Código** | **Tipo** | **Obrigatório** |
| --- | --- | --- |
| `conteudo_pronto` | string | Não |
| `materiais_existentes` | string | Não |
| `possui_identidade` | boolean | Não |
| `possui_logo` | boolean | Não |
| `cores_marca` | string | Não |
| `estilo_desejado` | array | Não |
| `sites_gosta` | string | Não |
| `concorrentes` | string | Não |

### **Grupo 5 - Prazo e Orçamento**

| **Código** | **Tipo** | **Obrigatório** |
| --- | --- | --- |
| `precisa_seo` | boolean | Não |
| `precisa_analytics` | boolean | Não |
| `data_estimada` | date | Não |
| `tem_urgencia` | boolean | Não |
| `orcamento_sugerido` | number | Não |
| `observacoes_finais` | string | Não |

### **Perguntas Específicas (condicionais)**

| **Código** | **Tipo** | **Quando usar** |
| --- | --- | --- |
| `ecommerce_produtos` | number | tipo_projeto = `ecommerce` |
| `ecommerce_pagamento` | array | tipo_projeto = `ecommerce` |
| `ecommerce_frete` | boolean | tipo_projeto = `ecommerce` |
| `institucional_paginas` | number | tipo_projeto = `institucional` |
| `institucional_blog` | boolean | tipo_projeto = `institucional` |
| `precisa_erp` | string | precisa_integracao = `true` |
| `precisa_crm` | string | precisa_integracao = `true` |

---

## **Formatos de Resposta por Tipo de Campo**

### **Texto curto (text)**

json

```
{
  "codigo": "texto simples"
}
```

### **Texto longo (textarea)**

json

```
{
  "codigo": "texto longo com múltiplas linhas\nsegunda linha"
}
```

### **Email**

json

```
{
  "email": "usuario@exemplo.com"
}
```

### **Número (number)**

json

```
{
  "ecommerce_produtos": 150
}
```

### **Data (date)**

json

```
{
  "data_estimada": "2025-12-31"
}
```

### **Seleção única (radio/select)**

json

```
{
  "tipo_projeto": "ecommerce"
}
```

### **Múltipla escolha (checkbox)**

json

```
{
  "finalidade": ["apresentar empresa", "captar leads", "vender"]
}
```

---

## **Exemplo Completo de Payload**

json

```
{
  "projeto_id": 42,
  "data_inicio": "2025-06-15T10:30:00Z",
  "versao_briefing": 1,
  "respostas": {
    "nome_empresa": "Cafeteria do João",
    "nome_projeto": "Site da Cafeteria",
    "responsavel": "João Silva",
    "email": "joao@cafeteria.com",
    "telefone": "(11) 99999-9999",
    "segmento": "cafeteria especializada",
    "tipo_projeto": "ecommerce",
    "principal_objetivo": "Vender café online",
    "publico_principal": "Jovens adultos 20-40 anos",
    "funcionalidades": ["login/cadastro", "pagamentos", "busca"],
    "ecommerce_produtos": 50,
    "ecommerce_pagamento": ["pix", "cartao_credito", "boleto"],
    "ecommerce_frete": true,
    "possui_identidade": true,
    "cores_marca": "#8B4513, #D2B48C",
    "data_estimada": "2025-08-30",
    "orcamento_sugerido": 15000
  },
  "status": "em_briefing",
  "ultima_atualizacao": "2025-06-15T14:45:00Z"
}
```

---

## **Validação de Dados**

### **Regras de Validação**

| **Campo** | **Regra** |
| --- | --- |
| `email` | Deve conter @ e domínio válido |
| `telefone` | Mínimo 10 caracteres |
| `data_estimada` | Não pode ser anterior à data atual |
| `orcamento_sugerido` | Deve ser maior que 0 |
| `ecommerce_produtos` | Mínimo 1, máximo 999999 |

### **Regras Condicionais**

| **Condição** | **Ação** |
| --- | --- |
| tipo_projeto = `ecommerce` | Campos ecommerce_* são obrigatórios |
| tipo_projeto = `institucional` | Campos institucional_* são obrigatórios |
| precisa_integracao = `true` | quais_sistemas deve ser preenchido |

---

## **Versionamento**

| **Versão** | **Data** | **Mudanças** |
| --- | --- | --- |
| 1.0 | 2025-06-15 | Versão inicial com todos os grupos |

---

## **Histórico de Revisão**

| **Data** | **Autor** | **Descrição** |
| --- | --- | --- |
| 2025-06-15 | Netz Team | Criação do documento |

---

## **Referências**

- models.py - Definição dos modelos Django
- seed_perguntas.py - Lista completa de perguntas
- design.md - Especificação visual do sistema

text

---

## Resumo:

| Seção | O que define |
|-------|--------------|
| Convenções de nomenclatura | Como nomear campos (`snake_case`) |
| Tipos de dados | string, number, boolean, array, object |
| Estrutura do Projeto | Campos principais e seus tipos |
| Status e tipos | Valores permitidos para status e tipo_projeto |
| Códigos de perguntas | Lista de todos os códigos por grupo |
| Formatos de resposta | Como cada tipo de campo deve ser enviado |
| Exemplo completo | Payload real para uma cafeteria |
| Validação | Regras de negócio para cada campo |
