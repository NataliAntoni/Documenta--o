`# Dev Workflow - Portal de Parcerias Netz

## Versão

1.0

---

## Visão Geral do Fluxo`

Briefing → Análise IA → Validação Técnica → Orçamento → Aprovação → Desenvolvimento → Homologação → Deploy → Pós-entrega

text

```

---

## Etapa 1: Recebimento do Briefing

### 1.1 Início do Processo

| Ação | Responsável | Tempo estimado |
|------|-------------|----------------|
| Cliente acessa o portal | Cliente/Agência | 1 min |
| Seleciona "Novo Briefing" | Cliente/Agência | - |
| Preenche os 5 grupos do formulário | Cliente/Agência | 15-30 min |

### 1.2 Durante o Preenchimento

| Ação | Descrição |
|------|-----------|
| IA analisa respostas em tempo real | Identifica nicho e sugere perguntas relevantes |
| Progresso é salvo automaticamente | Usuário pode voltar depois |
| Validação de campos obrigatórios | Impede avanço sem preenchimento |

### 1.3 Conclusão do Briefing

| Ação | Responsável | Descrição |
|------|-------------|-----------|
| Usuário finaliza o briefing | Cliente/Agência | Clica em "Concluir Briefing" |
| Sistema gera protocolo | Automático | Número do projeto é exibido |
| Notificação enviada | Automático | Email para equipe Netz |
| Briefing fica disponível em `/projetos/` | Sistema | Para consulta futura |

---

## Etapa 2: Análise da IA e Estruturação dos Dados

### 2.1 Processamento Automático

| Ação | Descrição |
|------|-----------|
| Extrair respostas do `briefing_json` | Todos os campos e valores |
| Identificar tipo de projeto | institucional, ecommerce, portal, etc. |
| Identificar nicho/segmento | cafeteria, moda, tecnologia, etc. |
| Mapear funcionalidades solicitadas | Login, pagamentos, integrações, etc. |
| Calcular complexidade | Baseado no número de perguntas respondidas |

### 2.2 Saída da IA

```json
{
  "tipo_projeto": "ecommerce",
  "nicho": "cafeteria especializada",
  "complexidade": "media",
  "funcionalidades_identificadas": ["pagamentos", "catalogo", "frete"],
  "sugestoes_tecnicas": ["WordPress + WooCommerce", "API de pagamento"],
  "tempo_estimado_dias": 45,
  "orcamento_sugerido": 15000
}
```

---

## **Etapa 3: Validação Técnica**

### **3.1 Revisão Manual pela Equipe Netz**

| **Ação** | **Responsável** | **Tempo estimado** |
| --- | --- | --- |
| Validar dados do briefing | Analista Netz | 15 min |
| Verificar viabilidade técnica | Dev Lead | 10 min |
| Identificar dependências externas | Analista | 5 min |
| Definir stack tecnológica | Dev Lead | 10 min |

### **3.2 Checkpoints de Validação**

| **Critério** | **O que verificar** |
| --- | --- |
| Clareza das respostas | Respostas vagas ou contraditórias? |
| Escopo definido | Funcionalidades claras? |
| Prazo realista | Entrega compatível com complexidade? |
| Orçamento viável | Cobre os custos do projeto? |

### **3.3 Se informações incompletas**

| **Ação** | **Descrição** |
| --- | --- |
| Marcar briefing como "pendente" | Status: `aguardando_cliente` |
| Enviar email para cliente | Lista de perguntas específicas |
| Cliente responde via portal | Mesmo fluxo do briefing |

---

## **Etapa 4: Geração e Envio do Orçamento**

### **4.1 Cálculo do Orçamento**

| **Fator** | **Peso** | **Como calcular** |
| --- | --- | --- |
| Tipo de projeto | 20% | ecommerce > institucional |
| Número de funcionalidades | 25% | Cada feature adiciona valor |
| Prazo | 15% | Urgência aumenta custo |
| Complexidade técnica | 25% | Integrações, APIs, etc. |
| Design | 15% | Customizado vs template |

### **4.2 Estrutura do Orçamento**

markdown

```
# Proposta Técnica e Comercial

## Resumo do Projeto
- Nome: {nome_projeto}
- Tipo: {tipo_projeto}
- Nicho: {segmento}

## Escopo Técnico
- Tecnologias: {stack_definida}
- Funcionalidades: {lista_funcionalidades}
- Prazo estimado: {prazo_dias} dias

## Investimento
- Desenvolvimento: R$ {valor_desenvolvimento}
- Design: R$ {valor_design}
- Integrações: R$ {valor_integracoes}
- **Total: R$ {valor_total}**

## Condições de Pagamento
- 30% na assinatura
- 40% na entrega da homologação
- 30% no deploy em produção
```

### **4.3 Envio da Proposta**

| **Ação** | **Responsável** | **Prazo** |
| --- | --- | --- |
| Gerar PDF da proposta | Sistema | Automático |
| Revisão final | Comercial Netz | 2 horas |
| Enviar para cliente | Comercial | - |
| Aguardar retorno | Cliente | Até 5 dias |

---

## **Etapa 5: Aprovação ou Revisão**

### **5.1 Cliente Aprova**

| **Ação** | **Descrição** |
| --- | --- |
| Cliente aceita proposta | Assina digitalmente |
| Status muda para `aprovado` | No sistema |
| Projeto entra na fila de desenvolvimento | Equipe alocada |

### **5.2 Cliente Solicita Ajustes**

| **Ação** | **Descrição** |
| --- | --- |
| Cliente envia solicitação de ajuste | Comentários no portal |
| Equipe Netz revisa | Negocia escopo |
| Nova proposta gerada | Enviada para cliente |

### **5.3 Cliente Rejeita**

| **Ação** | **Descrição** |
| --- | --- |
| Status muda para `cancelado` | Projeto arquivado |
| Motivo registrado | Para análise de melhoria |
| Briefing mantido no histórico | Disponível para consulta |

---

## **Etapa 6: Desenvolvimento**

### **6.1 Configuração do Ambiente**

| **Ação** | **Ferramenta** | **Responsável** |
| --- | --- | --- |
| Criar repositório | GitHub/GitLab | Dev Lead |
| Configurar ambiente de desenvolvimento | Docker/Local | Desenvolvedor |
| Instalar dependências | pip/npm | Desenvolvedor |
| Configurar banco de dados | PostgreSQL/MySQL | Desenvolvedor |

### **6.2 Estrutura de Branches**

text

```
main (produção)
  ↑
homolog (validação cliente)
  ↑
develop (integração)
  ↑
feature/* (novas funcionalidades)
```

### **6.3 Cronograma de Entregas**

| **Fase** | **Duração** | **Entregável** |
| --- | --- | --- |
| Setup inicial | 1 dia | Ambiente pronto |
| Desenvolvimento backend | 30% do prazo | APIs, admin |
| Desenvolvimento frontend | 40% do prazo | Telas, responsividade |
| Integrações | 20% do prazo | APIs externas |
| Testes | 10% do prazo | Correção de bugs |

### **6.4 Checkpoints Diários**

| **Horário** | **Atividade** |
| --- | --- |
| 10h | Daily de 15 min com a equipe |
| 15h | Commit do progresso no repositório |
| 18h | Atualização do projeto no portal (cliente visualiza) |

---

## **Etapa 7: Homologação**

### **7.1 Ambiente de Homologação**

| **Característica** | **Descrição** |
| --- | --- |
| URL | `homolog.seuprojeto.netz.com` |
| Acesso | Cliente + Equipe Netz |
| Protegido por senha | Somente usuários autorizados |

### **7.2 Checklist de Homologação**

| **Item** | **Critério** |
| --- | --- |
| Funcionalidades | Todas as especificadas no briefing |
| Responsividade | Funciona em desktop, tablet, mobile |
| Performance | Carregamento < 3 segundos |
| Acessibilidade | Segue WCAG 2.1 AA |
| SEO | Configurações básicas aplicadas |
| Segurança | HTTPS, proteção contra XSS/CSRF |

### **7.3 Validação pelo Cliente**

| **Ação** | **Prazo** | **Consequência se não responder** |
| --- | --- | --- |
| Cliente testa o site | 3 dias | Prazo prorrogado |
| Envia lista de ajustes | - | Equipe corrige |
| Aprova homologação | - | Segue para produção |

---

## **Etapa 8: Deploy em Produção**

### **8.1 Pré-Deploy**

| **Ação** | **Descrição** |
| --- | --- |
| Backup do ambiente de homologação | Cópia de segurança |
| Revisão final de código | Code review |
| Executar testes automatizados | Unitários e integração |
| Verificar variáveis de ambiente | Todas configuradas |

### **8.2 Deploy**

bash

```
# Fluxo de deploy
git checkout main
git merge homolog
git push origin main

# Executar migrações
python manage.py migrate --noinput

# Coletar arquivos estáticos
python manage.py collectstatic --noinput

# Reiniciar serviços
sudo systemctl restart gunicorn
sudo systemctl restart nginx
```

### **8.3 Pós-Deploy**

| **Ação** | **Responsável** |
| --- | --- |
| Testar site em produção | QA |
| Verificar logs de erro | Dev Lead |
| Notificar cliente | Comercial |
| Status muda para `concluido` | Sistema |

---

## **Etapa 9: Pós-Entrega**

### **9.1 Entrega ao Cliente**

| **Entregável** | **Formato** |
| --- | --- |
| Acesso ao site | URL e credenciais |
| Documentação técnica | PDF/Markdown |
| Manual do usuário | PDF/Video |
| Acesso ao código (se contratado) | Repositório privado |

### **9.2 Treinamento (se aplicável)**

| **Tipo** | **Duração** | **Conteúdo** |
| --- | --- | --- |
| Básico | 1 hora | Como editar conteúdo |
| Avançado | 2 horas | Painel administrativo, relatórios |
| Técnico | 3 horas | API, integrações, manutenção |

### **9.3 Suporte Pós-Entrega**

| **Período** | **Cobertura** | **Valor** |
| --- | --- | --- |
| Primeiros 30 dias | Correção de bugs | Incluso |
| Primeiro ano | Suporte por ticket | R$ 200/mês |
| Após 1 ano | Novo contrato | A combinar |

### **9.4 Encerramento do Projeto**

| **Ação** | **Responsável** |
| --- | --- |
| Arquivar documentação | Admin |
| Encerrar ambiente de homologação | DevOps |
| Atualizar portfólio da Netz | Marketing |
| Solicitar depoimento/referência | Comercial |

---

## **Fluxograma Resumido**

text

```
┌─────────────────┐
│  Briefing preenchido  │
└────────┬────────┘
         ↓
┌─────────────────┐
│   IA analisa dados    │
└────────┬────────┘
         ↓
┌─────────────────┐
│ Equipe Netz valida    │
└────────┬────────┘
         ↓
┌─────────────────┐
│  Gera orçamento      │
└────────┬────────┘
         ↓
┌─────────────────┐
│  Cliente aprova?     │
└────────┬────────┘
      ↓        ↓
     SIM      NÃO
      ↓        ↓
┌─────────┐  ┌─────────┐
│Desenvolve│  │Revisa/   │
│         │  │Cancela   │
└────┬────┘  └─────────┘
     ↓
┌─────────────────┐
│   Homologação     │
└────────┬────────┘
         ↓
┌─────────────────┐
│   Deploy produção  │
└────────┬────────┘
         ↓
┌─────────────────┐
│  Pós-entrega      │
└─────────────────┘
```

---

## **Responsáveis e Papéis**

| **Papel** | **Responsabilidades** |
| --- | --- |
| **Cliente/Agência** | Preenche briefing, aprova orçamento, valida homologação |
| **Analista Netz** | Valida briefing, negocia escopo, mantém cliente informado |
| **Dev Lead Netz** | Define stack, revisa código, garante qualidade técnica |
| **Desenvolvedor** | Codifica funcionalidades, corrige bugs |
| **QA** | Testa funcionalidades, reporta bugs |
| **DevOps** | Configura ambientes, faz deploy |
| **Comercial** | Envia proposta, fecha contrato |

---

## **Ferramentas Utilizadas**

| **Etapa** | **Ferramenta** |
| --- | --- |
| Briefing | Portal Django |
| Comunicação | Slack, Email |
| Repositório | GitHub/GitLab |
| Gerenciamento de projeto | Trello/ClickUp |
| Design | Figma |
| Ambiente de desenvolvimento | Docker |
| Deploy | Gunicorn + Nginx |
| Monitoramento | Sentry, Logs |

---

## **Histórico de Revisão**

| **Versão** | **Data** | **Autor** | **Descrição** |
| --- | --- | --- | --- |
| 1.0 | 2025-06-15 | Netz Team | Versão inicial do workflow |

text

```

---

## Resumo do Documento:

| Seção | Conteúdo |
|-------|----------|
| Etapa 1 | Recebimento do briefing pelo cliente |
| Etapa 2 | IA analisa e estrutura os dados |
| Etapa 3 | Equipe Netz valida tecnicamente |
| Etapa 4 | Geração e envio do orçamento |
| Etapa 5 | Cliente aprova ou pede revisão |
| Etapa 6 | Desenvolvimento do projeto |
| Etapa 7 | Homologação com cliente |
| Etapa 8 | Deploy em produção |
| Etapa 9 | Entrega e suporte pós-lançamento |
```