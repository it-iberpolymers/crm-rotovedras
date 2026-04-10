<p align="center">
  <img src="https://raw.githubusercontent.com/YOUR_USER/YOUR_REPO/main/logo.png" alt="Rotovedras" width="280">
</p>

<h3 align="center">Plataforma de Gestão Operacional</h3>

<p align="center">
  Mockup interativo da implementação Monday.com para o Grupo Iberpolymers
</p>

<p align="center">
  <img src="https://img.shields.io/badge/versão-2.1-509ECB?style=flat-square" alt="Version">
  <img src="https://img.shields.io/badge/monday.com-mockup-509ECB?style=flat-square" alt="Monday.com">
  <img src="https://img.shields.io/badge/deploy-Vercel-black?style=flat-square" alt="Vercel">
</p>

---

## Sobre

Protótipo funcional em HTML/JS da plataforma de gestão transversal da **Rotovedras** (Grupo Iberpolymers), desenhado como referência para a implementação no Monday.com.

A aplicação simula a experiência completa de um Work OS industrial — desde a gestão comercial até à produção — num único ficheiro `index.html` pronto para deploy.

## Módulos

### CRM (funcional)

| Área | Descrição |
|------|-----------|
| **Dashboard** | KPIs, gráficos pipeline, funil, leads por canal, performance comercial |
| **Leads** | 12 leads com estados, canais, pesquisa, formulário de adição |
| **Contactos** | Registo de contactos com cargo, notas, ligação a leads |
| **Oportunidades** | Pipeline 6 estágios + Fechado (Ganho/Perdido), vista tabela + Kanban |
| **Propostas** | Propostas com linhas de artigo, cálculo automático de preços/margens/IVA |
| **Clientes** | Classificação Prospect → Potencial → Ativo, volume acumulado |
| **Classificação** | Calculadora A/B/C/D com critérios ponderados (cliente atual e novo) |
| **Moldes & Produtos** | Registo de moldes (propriedade cliente), fichas produto, catálogo serviços |
| **Colaboradores** | Equipa com avatar, departamento, métricas de pipeline por comercial |

### Produção (funcional)

| Área | Descrição |
|------|-----------|
| **Ordens de Fabrico** | 8 OFs em 9 estágios, alocação unidade/forno/braço |
| **Planeamento** | Vista hierárquica U1 Torres Vedras → U2 Casalinhos → U3 Paúl, ocupação por braço |
| **Estado Produção** | Painel tablet com cards de OFs em curso e barra de progresso |
| **Acabamentos** | Checklist dinâmica por OF (corte, montagem, soldadura, pintura, testes) |
| **Guias Montagem** | Passos sequenciais por produto para formalizar conhecimento operacional |

### Áreas em construção (menu criado)

- **Estrutura Produto** — Artigos, BOM
- **Stock** — Inventário
- **Operações** — Encomendas cliente, Encomendas internas
- **Supply Chain** — Compras, Compras engenharia, Logística
- **Engenharia** — Projetos (Fase 0–3)
- **Qualidade** — Receção, Não conformidades, Auditorias
- **IT** — Suporte, Políticas, FAQs, Aquisição equipamentos
- **Comunicação** — Fichas técnicas, Catálogos, Merchandising
- **Financeiro** — Faturação, Receber, Pagar, Margens
- **Concursos públicos**

## Contexto operacional

| | |
|---|---|
| **Grupo** | Iberpolymers (Rotovedras, Ambiconcept, Waterpor, Buildpor) |
| **Atividade** | Rotomoldagem — produção por encomenda |
| **Unidades** | 3 unidades industriais (Torres Vedras, Casalinhos, Paúl) |
| **Capacidade** | 8 fornos, 16 braços produtivos |
| **Modelo** | O cliente é dono do molde; a Rotovedras vende capacidade produtiva |
| **ERP** | Winmax (integração futura via API) |
| **Consultoria** | ADNEW (Lethycia Wust) |

## Oportunidades — pipeline comercial

```
Nova oportunidade → Proposta em preparação → Proposta enviada
→ Aguardando decisão → Adjudicado → Fechado (Ganho / Perdido)
```

## Propostas — estrutura de linhas

Cada proposta contém linhas de artigo com cálculo automático:

- **Preço unitário** = Custo × (1 + Margem%) × (1 − Desconto%)
- **Valor linha** = Preço unitário × Quantidade
- **Valor c/ IVA** = Valor linha × (1 + IVA%)

## Classificação de clientes

Dois modos (atual e novo), score 0–100 com classificação:

| Classe | Score | Descrição |
|--------|-------|-----------|
| **A** | ≥ 80 | Premium |
| **B** | ≥ 60 | Standard |
| **C** | ≥ 30 | Básico |
| **D** | < 30 | Risco |

## Serviços Rotovedras

1. Desenvolvimento de Produto
2. Desenvolvimento de Molde
3. Produção de Molde
4. Produção de Produto
5. Protótipo
6. Engenharia Inversa

## Stack técnico

- **HTML/CSS/JS** — ficheiro único, zero dependências de build
- **Chart.js 4.4** — gráficos do dashboard
- **DM Sans** — tipografia (Google Fonts)
- Logo embedido em base64

## Deploy

### Vercel (drag & drop)

1. Vai a [vercel.com/new](https://vercel.com/new)
2. Arrasta a pasta com o `index.html`
3. Deploy automático

### GitHub Pages

1. Push para um repo
2. Settings → Pages → Source: main branch
3. O site fica disponível em `username.github.io/repo`

### Local

Basta abrir `index.html` no browser.

## Estrutura

```
/
├── index.html    ← aplicação completa (single-file)
├── logo.png      ← logotipo Rotovedras
└── README.md
```

## Roadmap

- [ ] Desenvolver módulos placeholder (Supply Chain, Engenharia, Qualidade, etc.)
- [ ] Formulário completo de criação de OF
- [ ] Geração automática de encomendas a partir de propostas adjudicadas
- [ ] Integração API Winmax (middleware Make/Zapier)
- [ ] Migração de estrutura para Monday.com real via MCP tools
- [ ] Vista Gantt para planeamento de produção
- [ ] Registo de produção via tablet (operadores)

---

<p align="center">
  <strong>Rotovedras</strong> · Plastic Technology<br>
  <sub>Grupo Iberpolymers © 2026</sub>
</p>
