---
description: # Guia de Implementação e Validação de Fluxos
---

## CRM Simplificado para Salões de Beleza

**Objetivo:** definir a ordem exata de desenvolvimento do produto e validar fluxos reais em ambiente de salão antes de escalar.

---

# Filosofia do Desenvolvimento

O produto deve ser construído em camadas incrementais.

Cada etapa precisa funcionar sozinha como produto utilizável.

Antes de avançar, a etapa atual deve estar:

* funcionando em produção (mobile Android/iOS)
* testada em uso real (não só simulado)
* utilizada por pelo menos 1 salão piloto por alguns dias
* estável o suficiente para operação diária

Sem isso, não existe “pronto”.

---

# Etapa 0 — Fundação Técnica (Mobile)

## Objetivo

Criar base do aplicativo mobile e backend.

## Features

### FEAT-001 — Setup do App Mobile

* React Native (Expo)
* TypeScript
* Navegação base
* Estrutura de pastas
* Configuração de build (EAS)

---

### FEAT-002 — Backend Inicial

Entidades base:

* User
* Salon
* Client
* Professional
* Appointment
* ServiceHistory

---

### FEAT-003 — Infraestrutura

* PostgreSQL
* Prisma
* Docker
* Deploy backend (Railway/Render)
* Storage (imagens)

---

## Critério para avançar

App abre no Android e iOS e consegue conectar no backend em produção.

---

# Etapa 1 — Autenticação (MVP)

## Objetivo

Permitir uso seguro no app real.

## Ordem

### FEAT-004 — Cadastro

### FEAT-005 — Login

### FEAT-006 — Recuperação de senha

### FEAT-007 — Persistência de sessão

### FEAT-008 — Isolamento por salão (multi-tenant)

---

## Fluxo de validação real

```text
Instalar app
↓
Criar conta
↓
Fazer login
↓
Fechar app
↓
Abrir novamente
↓
Continuar logado
```

---

## Critério para avançar

Usuário consegue entrar no app sem suporte técnico.

Se precisar de ajuda → não está pronto.

---

# Etapa 2 — Clientes (MVP)

## Objetivo

Substituir o caderno físico.

## Ordem

### FEAT-009 — Criar cliente

### FEAT-010 — Listar clientes

### FEAT-011 — Buscar clientes

### FEAT-012 — Editar cliente

### FEAT-013 — Remover cliente

---

## Fluxo de validação real

```text
Abrir app
↓
Cadastrar cliente na hora do atendimento
↓
Sair da tela
↓
Encontrar cliente depois em segundos
```

---

## Critério para avançar

O salão para de usar caderno (mesmo parcialmente).

---

# Etapa 3 — Histórico de Atendimento

## Objetivo

Capturar o valor central do produto.

## Ordem

### FEAT-014 — Registrar atendimento

### FEAT-015 — Timeline do cliente

### FEAT-016 — Tela de perfil do cliente

---

## Fluxo de validação real

```text
Cliente atende
↓
Registrar atendimento imediatamente
↓
Voltar depois e ver histórico completo
```

---

## Critério para avançar

Profissional usa isso durante atendimento real sem atrito.

Se for mais lento que papel → falhou.

---

# Etapa 4 — Profissionais

## Objetivo

Permitir operação em equipe.

## Ordem

### FEAT-017 — Cadastro profissional

### FEAT-018 — Edição

### FEAT-019 — Associação atendimento ↔ profissional

---

## Fluxo de validação

```text
Criar profissional
↓
Registrar atendimento
↓
Selecionar responsável
```

---

## Critério

Equipe consegue operar sem confusão de registros.

---

# Etapa 5 — Agenda

## Objetivo

Organização operacional real.

## Ordem

### FEAT-020 — Criar agendamento

### FEAT-021 — Agenda diária

### FEAT-022 — Agenda semanal

### FEAT-023 — Editar

### FEAT-024 — Cancelar

---

## Fluxo de validação real

```text
Agendar cliente
↓
Consultar agenda durante o dia
↓
Alterar horário quando necessário
```

---

## Critério

Salão usa agenda diariamente por 3 dias seguidos sem voltar para papel.

---

# Etapa 6 — Dashboard

## Objetivo

Visão rápida do negócio.

## Ordem

### FEAT-025 — Indicadores

### FEAT-026 — Atendimentos recentes

---

## Fluxo de validação

Usuário abre app e entende o dia do salão sem navegar.

---

## Critério

Decisão operacional pode ser tomada só olhando essa tela.

---

# Etapa 7 — Retenção

## Objetivo

Valor diferencial do produto.

## Ordem

### FEAT-027 — Configuração de retorno

### FEAT-028 — Detecção de inatividade

### FEAT-029 — Lista de clientes inativos

### FEAT-030 — Ordenação por urgência

---

## Fluxo de validação real

```text
Cliente some
↓
Sistema identifica
↓
Usuário confirma manualmente
```

---

## Critério

Sem falso negativo (cliente esquecido pelo sistema).

---

# Etapa 8 — WhatsApp

## Objetivo

Fechar ciclo de retenção.

## Ordem

### FEAT-031 — Link WhatsApp

### FEAT-032 — Templates

### FEAT-033 — Abrir conversa

---

## Fluxo de validação

```text
Cliente inativa aparece
↓
Usuário toca em "enviar mensagem"
↓
WhatsApp abre pronto
```

---

## Critério

Fluxo leva menos tempo que digitar manualmente no WhatsApp.

---

# MVP FINAL

Se chegou aqui:

* app funciona no dia a dia real
* salão usa sem suporte constante
* substitui pelo menos parte do processo manual

Só então:

→ cobrar
→ escalar
→ vender

---

# Versão 1.1

### FEAT-034 — Ficha técnica (coloração)

### FEAT-035 — Upload de fotos

### FEAT-036 — Relatórios simples

### FEAT-037 — Exportação PDF

### FEAT-038 — Filtros avançados

---

# Versão 1.2

### FEAT-039 — Convite de equipe

### FEAT-040 — Permissões

### FEAT-041 — Auditoria básica

### FEAT-042 — Onboarding guiado

### FEAT-043 — Importação CSV

---

# Versão 2.0

### FEAT-044 — Push notifications

### FEAT-045 — Campanhas de retenção

### FEAT-046 — Automação de mensagens

### FEAT-047 — Segmentação

### FEAT-048 — Aniversariantes

### FEAT-049 — Funil de retenção

---

# Versão 3.0

### FEAT-050 — App mais polido (iOS/Android)

### FEAT-051 — Pagamentos (Mercado Pago)

### FEAT-052 — Assinaturas

### FEAT-053 — Agendamento público

### FEAT-054 — Confirmação automática

### FEAT-055 — Integração Instagram

---

# Versão Escala

### FEAT-056 — IA de retenção

### FEAT-057 — Dashboard financeiro

### FEAT-058 — CRM avançado

### FEAT-059 — BI analytics

### FEAT-060 — Marketplace

### FEAT-061 — API pública

---

# Ordem resumida

```text
Infraestrutura mobile
↓
Autenticação
↓
Clientes
↓
Histórico
↓
Profissionais
↓
Agenda
↓
Dashboard
↓
Retenção
↓
WhatsApp
====================
MVP REAL USÁVEL
====================
```

---

# Regra final (a única que importa)

Se um salão não consegue usar isso durante um dia inteiro sem te chamar:

não é produto.

é só código organizado tentando parecer útil.
