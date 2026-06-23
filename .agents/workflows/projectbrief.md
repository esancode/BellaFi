---
description: # Project Brief — CRM Mobile para Salões de Beleza
---

## 1. Nome do Produto

BellaFi

---

## 2. Resumo do Projeto

Aplicativo mobile nativo para Android e iOS voltado para gestão operacional de pequenos salões de beleza.

O foco não é “software de gestão completo”, e sim um sistema extremamente simples que substitui cadernos, planilhas e memória informal do salão.

O produto centraliza clientes, histórico de atendimentos, agenda e mecanismos básicos de retenção.

---

## 3. Problema

Pequenos salões operam com ferramentas fragmentadas:

* caderno físico para clientes
* WhatsApp para comunicação
* memória dos profissionais para histórico
* nenhuma visão de recorrência real

Isso gera:

* perda de clientes por falta de retorno
* ausência de histórico confiável
* agendamentos desorganizados
* baixa previsibilidade de receita
* dependência de memória humana

O problema real não é “falta de software”, é falta de sistema simples o suficiente para ser usado diariamente.

---

## 4. Solução Proposta

Um app mobile que funciona como “caderno inteligente do salão”, com quatro pilares:

* Clientes centralizados
* Histórico de atendimentos sempre acessível
* Agenda simples e rápida
* Sistema automático de retenção (clientes que sumiram)

Tudo projetado para uso em tempo real durante o atendimento.

---

## 5. Objetivos do Produto

### Objetivos principais

* Substituir caderno físico do salão
* Centralizar histórico de clientes
* Aumentar recorrência de clientes
* Organizar agenda sem complexidade
* Reduzir perda de clientes por esquecimento

### Objetivos secundários

* Permitir operação em equipe
* Facilitar comunicação via WhatsApp
* Criar base para automações futuras

---

## 6. Público-Alvo

### Primário

Dona de salão pequeno

* 30–55 anos
* baixa afinidade tecnológica
* usa WhatsApp como principal ferramenta digital
* trabalha sozinha ou com equipe pequena

### Secundário

Salões pequenos com equipe

* 2 a 5 profissionais
* necessidade de organização compartilhada
* busca controle básico de operação

---

## 7. Proposta de Valor

“Um sistema que o salão realmente usa todos os dias, sem precisar aprender tecnologia.”

Diferencial real:

* não é complexo
* não depende de treinamento
* funciona em fluxo de atendimento real
* resolve recorrência, não só cadastro

---

## 8. Escopo do MVP

### Inclui

* Autenticação
* Gestão de clientes
* Histórico de atendimentos
* Agenda simples
* Cadastro de profissionais
* Dashboard básico
* Sistema de clientes inativos
* Integração com WhatsApp (link)

---

### Não inclui (MVP)

* pagamentos
* push notifications
* automações avançadas
* BI completo
* marketplace
* agendamento público
* integrações externas complexas

---

## 9. Fluxo Principal do Produto

Fluxo diário real esperado:

```text
Abrir app
↓
Ver agenda do dia
↓
Atender cliente
↓
Registrar atendimento em segundos
↓
Sair da tela
↓
Depois consultar histórico ou próximo agendamento
```

Fluxo de retenção:

```text
Sistema identifica cliente ausente
↓
Usuário vê lista
↓
Clica em WhatsApp
↓
Cliente é reativado manualmente
```

---

## 10. Métricas de Sucesso

### Adoção

* usuário cria primeiro cliente em < 5 minutos
* usuário registra primeiro atendimento em < 2 minutos

### Retenção

* > 80% de retenção mensal em salões piloto

### Uso real

* sistema substitui parcialmente caderno em > 70% dos salões

### Negócio

* disposição clara de pagamento recorrente
* churn < 5% ao mês em early adopters

---

## 11. Premissas do Produto

* simplicidade vence complexidade
* salão não quer “software”, quer “controle”
* uso real importa mais que features
* se for mais lento que papel, falhou
* WhatsApp continuará sendo ferramenta externa principal

---

## 12. Restrições Técnicas

* foco total em mobile (Android e iOS)
* backend simples e escalável
* offline parcial desejável (cache básico)
* performance crítica (uso durante atendimento)

---

## 13. Stack Tecnológica

### Mobile

* React Native (Expo)
* TypeScript
* Zustand
* React Navigation

### Backend

* Node.js
* NestJS
* PostgreSQL
* Prisma

### Infraestrutura

* Docker
* Railway ou Render
* Supabase Storage
* EAS Build (Expo)

---

## 14. Riscos Principais

### Risco 1 — Complexidade excessiva

Se o sistema crescer além do necessário, usuários abandonam.

### Risco 2 — Adoção real baixa

Se não for usado no fluxo de atendimento, vira “software esquecido”.

### Risco 3 — Substituição incompleta do caderno

Se o app não substituir o papel parcialmente, não há retenção.

---

## 15. Critério de Sucesso do MVP

O produto só é validado se:

* pelo menos 10 salões usam por 30 dias reais
* uso diário acontece sem suporte constante
* clientes são registrados e consultados ativamente
* retenção supera uso de caderno em parte relevante do fluxo
* há disposição real de pagamento

---

## 16. Estratégia de Evolução

1. MVP ultra simples (uso diário real)
2. retenção (clientes sumidos)
3. comunicação (WhatsApp)
4. equipe e permissões
5. automações
6. pagamentos
7. escala

---

## 17. Definição de “Pronto”

O produto não está pronto quando funciona.

Está pronto quando:

* é usado sem incentivo externo
* faz parte da rotina do salão
* substitui comportamento antigo (caderno/WhatsApp manual)

---

Se quiser, posso transformar isso em:

* pitch para investidores
* one-pager de venda
* ou PRD técnico detalhado para equipe de dev
