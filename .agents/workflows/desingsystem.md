---
description: # CRM Salão de Beleza — Design System & CSS Requirements
---

Versão: 1.0
Status: Obrigatório
Escopo: Aplicativo Mobile (React Native / Expo)

---

# 1. Objetivo

Este documento define os padrões visuais obrigatórios do aplicativo.

Nenhuma tela poderá violar estas regras.

O objetivo é garantir:

* Consistência visual.
* Redução de carga cognitiva.
* Curva de aprendizado mínima.
* Facilidade de manutenção.
* Escalabilidade do produto.

Toda nova tela deverá reutilizar componentes existentes antes de criar novos.

---

# 2. Princípios Visuais

## 2.1 Prioridades

A interface deve transmitir:

1. Simplicidade.
2. Confiança.
3. Feminilidade premium.
4. Organização.
5. Rapidez.

Nunca transmitir:

* Complexidade corporativa.
* Aparência hospitalar.
* Visual "ERP antigo".
* Excesso de informação.
* Visual genérico de dashboard SaaS.

---

# 3. Grid e Layout

## Grid Base

Utilizar sistema baseado em múltiplos de 8.

Exemplos:

8px
16px
24px
32px
40px
48px

Nunca utilizar:

13px
17px
19px
27px

---

## Margens Globais

```css
padding-horizontal: 24px;
```

Mínimo permitido:

```css
16px
```

Máximo:

```css
32px
```

---

## Espaçamento Vertical

Entre componentes relacionados:

```css
8px ou 12px
```

Entre grupos:

```css
24px
```

Entre seções principais:

```css
40px
```

---

# 4. Cores

## Primária

```css
--color-primary: #D977A7;
```

Uso:

* CTA principal
* FAB
* Estados ativos
* Links importantes

---

## Primária Hover

```css
--color-primary-dark: #C05F92;
```

---

## Secundária

```css
--color-secondary: #F8E8F0;
```

Uso:

* Backgrounds suaves
* Cards destacados

---

## Destaque

```css
--color-accent: #7C3AED;
```

Uso:

* Badges especiais
* Indicadores premium

Nunca usar como CTA principal.

---

## Texto

```css
--color-text-primary: #1F2937;
--color-text-secondary: #6B7280;
--color-text-disabled: #9CA3AF;
```

---

## Fundo

```css
--color-background: #FFFFFF;
--color-surface: #FAFAFA;
```

---

## Estados

Sucesso:

```css
#22C55E
```

Erro:

```css
#EF4444
```

Aviso:

```css
#F59E0B
```

Informação:

```css
#3B82F6
```

---

# 5. Tipografia

## Família

Obrigatório:

```css
Inter
```

Fallback:

```css
System
```

---

# Escala Tipográfica

## H1

```css
font-size: 32px;
font-weight: 700;
line-height: 40px;
```

Uso:

* Títulos de onboarding.

---

## H2

```css
font-size: 24px;
font-weight: 700;
line-height: 32px;
```

Uso:

* Títulos de tela.

---

## H3

```css
font-size: 20px;
font-weight: 600;
line-height: 28px;
```

---

## Body Large

```css
font-size: 16px;
font-weight: 400;
line-height: 24px;
```

Texto padrão do sistema.

---

## Body Small

```css
font-size: 14px;
font-weight: 400;
line-height: 20px;
```

---

## Caption

```css
font-size: 12px;
font-weight: 500;
line-height: 16px;
```

---

Nunca utilizar:

```css
11px
13px
15px
```

---

# 6. Bordas

Padrão universal:

```css
border-radius: 16px;
```

---

## Inputs

```css
border-radius: 14px;
```

---

## Cards

```css
border-radius: 20px;
```

---

## Bottom Sheet

```css
border-radius: 28px 28px 0 0;
```

---

## FAB

```css
border-radius: 999px;
```

---

Nunca utilizar:

```css
0px
4px
6px
```

O produto deve parecer acolhedor.

---

# 7. Sombras

Sombras devem ser discretas.

## Card padrão

```css
shadow-color: #000;
shadow-opacity: 0.05;
shadow-radius: 8;
elevation: 2;
```

---

## Modal

```css
shadow-opacity: 0.10;
shadow-radius: 16;
elevation: 6;
```

---

Nunca usar:

Sombras fortes.

---

# 8. Botões

## Altura

```css
56px
```

Padrão obrigatório.

---

## CTA Primário

```css
background: primary;
text-color: white;
height: 56px;
radius: 16px;
font-size: 16px;
font-weight: 600;
```

Largura:

```css
100%
```

---

## CTA Secundário

```css
background: transparent;
border: 1px solid #E5E7EB;
```

---

## Botão Destrutivo

```css
background: #FEF2F2;
text: #EF4444;
```

---

# 9. Inputs

Altura:

```css
56px
```

Padding:

```css
16px
```

Borda:

```css
1px solid #E5E7EB
```

Focus:

```css
2px solid #D977A7
```

Erro:

```css
2px solid #EF4444
```

---

Placeholder:

```css
#9CA3AF
```

---

# 10. Cards

Todos os cards devem conter:

```css
padding: 16px;
gap: 8px;
radius: 20px;
```

Jamais usar cards sem padding.

---

# 11. Lista de Clientes

Altura mínima item:

```css
72px
```

Estrutura:

* Avatar.
* Nome.
* Informação secundária.
* Ação rápida.

---

# 12. Avatar

Padrão:

```css
48x48
```

Grande:

```css
72x72
```

---

# 13. Bottom Navigation

Altura:

```css
72px
```

Itens:

Máximo:

```css
5
```

Obrigatórios:

* Dashboard
* Clientes
* Agenda
* Retenção
* Configurações

---

# 14. Floating Action Button

Tamanho:

```css
64x64
```

Posição:

```css
bottom: 24px;
right: 24px;
```

---

# 15. Ícones

Biblioteca:

```css
Lucide Icons
```

Peso:

```css
2px stroke
```

Tamanho padrão:

```css
24px
```

Nunca misturar bibliotecas.

---

# 16. Estados Vazios

Toda tela sem conteúdo deve possuir:

* Ilustração simples.
* Texto explicativo.
* CTA primário.

Exemplo:

"Você ainda não cadastrou clientes."

Botão:

"Cadastrar cliente"

---

# 17. Loading

Até:

300ms

Sem indicador.

---

300ms–2s

Skeleton.

---

2s+

Spinner com texto.

---

Nunca utilizar spinner infinito silencioso.

---

# 18. Animações

Duração:

```css
200ms–300ms
```

Curva:

```css
ease-out
```

Permitido:

* Fade.
* Slide.
* Scale discreto.

Proibido:

* Bounce.
* Elastic.
* Rotações exageradas.

---

# 19. Acessibilidade

Touch target mínimo:

```css
48x48
```

Contraste mínimo:

WCAG AA.

Todo ícone interativo deve possuir label.

---

# 20. Regras de Consistência

Nenhuma tela pode:

* Criar nova cor.
* Criar novo radius.
* Criar novo botão.
* Criar nova tipografia.
* Criar novo padrão de sombra.

Toda exceção exige aprovação formal.

---

# 21. Componentes Obrigatórios

Todos devem ser reutilizáveis:

* Button
* Input
* Card
* Avatar
* Badge
* Modal
* BottomSheet
* FAB
* EmptyState
* SearchBar
* ClientCard
* MetricCard
* AppointmentCard
* ProfessionalCard

---

# 22. Filosofia Final

O usuário principal possui baixa afinidade tecnológica.

Se existir dúvida entre:

"mais bonito"

ou

"mais simples"

sempre escolher:

"mais simples".
