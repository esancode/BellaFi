---
description: # CRM Simplificado para Salões de Beleza  ## Documento de Levantamento de Requisitos (MVP)
---

**Versão:** 1.0
**Data:** Junho/2026
**Status:** Em definição

---

# 1. Visão Geral

Sistema CRM simplificado voltado para pequenos e médios salões de beleza, com foco em retenção de clientes, histórico de atendimentos e gestão simplificada da agenda.

Aplicativo mobile nativo para Android e iOS, com foco em simplicidade extrema e uso diário por profissionais com baixa familiaridade tecnológica.

---

# 2. Objetivos do Produto

* Centralizar informações dos clientes.
* Evitar perda de clientes por falta de acompanhamento.
* Facilitar o acesso ao histórico de atendimentos.
* Substituir cadernos, planilhas e anotações dispersas.
* Melhorar a retenção e recorrência dos clientes.
* Oferecer uma solução simples e acessível para pequenos salões.

---

# 3. Personas

## Persona Primária

**Dona de salão pequeno**

* Idade: 30-55 anos
* Pouca afinidade tecnológica
* Utiliza WhatsApp e cadernos físicos
* Trabalha sozinha ou com até 3 profissionais

## Persona Secundária

**Salão com sócias ou equipe**

* 2 a 5 profissionais
* Necessidade de compartilhamento de informações
* Busca maior controle operacional

---

# 4. Requisitos Funcionais

## RF01 - Autenticação

O sistema deverá permitir:

* Cadastro de usuários.
* Login via e-mail e senha.
* Recuperação de senha.
* Logout.

---

## RF02 - Cadastro de Clientes

O sistema deverá permitir:

* Cadastrar cliente.
* Editar cliente.
* Excluir cliente.
* Pesquisar cliente.

### Campos obrigatórios

* Nome completo.
* Telefone.

### Campos opcionais

* Data de nascimento.
* Observações livres.
* Foto do cliente.

---

## RF03 - Histórico de Atendimento

O sistema deverá permitir registrar atendimentos contendo:

* Cliente.
* Profissional responsável.
* Data do atendimento.
* Serviço realizado.
* Produtos utilizados.
* Valor cobrado.
* Observações.

O sistema deverá exibir:

* Histórico cronológico.
* Último atendimento.
* Valor médio gasto.

---

## RF04 - Agendamento Simples

O sistema deverá permitir:

* Criar agendamento.
* Editar agendamento.
* Cancelar agendamento.
* Visualizar agenda diária.
* Visualizar agenda semanal.

Cada profissional deverá possuir sua própria agenda.

Não haverá integração externa no MVP.

---

## RF05 - Gestão de Profissionais

O sistema deverá permitir:

* Cadastrar profissionais.
* Editar profissionais.
* Ativar/Inativar profissionais.
* Associar atendimentos a profissionais.

---

## RF06 - Alerta de Retorno

O sistema deverá:

* Permitir configurar prazo de retorno em dias.
* Identificar automaticamente clientes inativos.
* Exibir lista de clientes que não retornaram.

Exemplo:

```text
Cliente sem atendimento há mais de 60 dias.
```

---

## RF07 - Envio via WhatsApp

O sistema deverá:

* Gerar link pré-formatado para WhatsApp.
* Abrir conversa diretamente no aplicativo.

Exemplo:

```text
Olá Maria! Sentimos sua falta no salão.
Gostaria de agendar um horário?
```

Não haverá integração oficial com API do WhatsApp no MVP.

---

## RF08 - Dashboard Inicial

O sistema deverá apresentar:

* Total de clientes.
* Clientes inativos.
* Atendimentos do dia.
* Próximos agendamentos.

---

## RF09 - Relatórios Mensais

O sistema deverá gerar:

* Total de atendimentos.
* Faturamento estimado.
* Clientes novos cadastrados.
* Clientes recorrentes.

Exportação para PDF ficará para versões futuras.

---

# 5. Requisitos Não Funcionais

## RNF01 - Usabilidade

* O sistema deverá ser intuitivo.
* Usuários deverão conseguir operar sem treinamento formal.
* Fluxos críticos devem exigir no máximo 3 toques na interface.

---

## RNF02 - Performance

* Tempo máximo de carregamento: 2 segundos.
* Pesquisas devem responder em até 1 segundo.

---

## RNF03 - Plataforma

* O sistema deverá funcionar em:

  * Android
  * iOS

---

## RNF04 - Disponibilidade

* Disponibilidade mínima de 99,5% no backend.

---

## RNF05 - Segurança

* Senhas criptografadas.
* Comunicação HTTPS obrigatória.
* Autenticação protegida por JWT.
* Controle de acesso por usuário.

---

## RNF06 - Backup

* Backup automático diário.
* Recuperação de dados em caso de falha.

---

## RNF07 - Escalabilidade

Arquitetura preparada para:

* Até 10 mil clientes por salão.
* Até 100 profissionais por salão.

---

## RNF08 - Compatibilidade

* Android 8+.
* iOS 13+.

---

# 6. Regras de Negócio

## RN01

Todo atendimento deve estar associado a um cliente.

## RN02

Todo atendimento deve possuir um profissional responsável.

## RN03

Clientes não podem possuir telefones duplicados dentro do mesmo salão.

## RN04

Clientes serão considerados "inativos" quando ultrapassarem o prazo configurado sem novo atendimento.

## RN05

Somente usuários autenticados poderão acessar informações do salão.

## RN06

Cada salão visualizará apenas seus próprios dados (multitenancy).

---

# 7. MVP (Versão Inicial)

## Funcionalidades obrigatórias

### Clientes

* Cadastro
* Busca
* Edição

### Atendimentos

* Registro de serviços
* Histórico completo

### Agenda

* Agenda diária e semanal
* Agendamento manual

### Retenção

* Alerta de cliente inativo
* Lista de clientes para retorno

### Comunicação

* Link direto para WhatsApp

### Equipe

* Multi-profissional básico

### Dashboard

* Indicadores principais

---

## Fora do MVP

* Aplicativo web
* PWA
* Integração com pagamentos
* API oficial do WhatsApp
* Importação de dados
* Notificações push (fase futura)
* Automações avançadas
* Relatórios avançados
* Programa de fidelidade

---

# 8. Roadmap

## V1.1

* Ficha técnica de coloração
* Relatórios avançados
* Importação de clientes
* Exportação PDF
* Multiusuário avançado

## V2.0

* Melhorias no app Android e iOS
* Integração com pagamentos
* Notificações push
* Automação de campanhas

---

# 9. Stack Tecnológica

## Aplicativo Mobile (Frontend)

* React Native
* TypeScript
* Expo (managed workflow)
* React Navigation
* Zustand (estado global)
* Axios (API client)

## Backend

* Node.js
* NestJS

## Banco de Dados

* PostgreSQL

## ORM

* Prisma ORM

## Autenticação

* JWT + Refresh Token

## Infraestrutura

* Docker
* Railway ou Render (Backend)
* Supabase Storage (imagens e mídia)
* EAS Build (Expo Application Services) para builds Android e iOS
* Distribuição via Google Play Store e Apple App Store

---

# 10. Diretrizes de Design

## Conceitos

* Mobile First (100% foco em app)
* Interface minimalista
* Baixa curva de aprendizado
* Estética premium e feminina

## Princípios

* Poucos campos por tela
* Tipografia grande
* Fluxos rápidos
* Máximo de 3 ações por tarefa

## Cores sugeridas

### Primária

```text
#D977A7
```

### Secundária

```text
#F8E8F0
```

### Destaque

```text
#7C3AED
```

### Sucesso

```text
#22C55E
```

### Erro

```text
#EF4444
```

## Componentes principais

* Cards
* Calendário
* Bottom Navigation
* Floating Action Button
* Busca global
* Listas com filtros rápidos

---

# 11. Métricas de Sucesso

* Usuário cadastra primeiro cliente em menos de 5 minutos
* Usuário registra primeiro atendimento em menos de 2 minutos
* Retenção mensal superior a 80%
* Pelo menos 70% dos usuários utilizam alerta de retorno
* Churn inferior a 5% ao mês

---

# 12. Critérios de Aceite do MVP

O MVP será considerado validado quando:

* 10 salões utilizarem o sistema por pelo menos 30 dias
* Pelo menos 70% afirmarem que substituíram cadernos ou planilhas
* Pelo menos 50% enviarem mensagens de retorno pelo sistema
* Houver disposição real de pagamento recorrente
* NPS superior a 8
