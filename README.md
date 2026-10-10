# Tech Challenge — Fase 1: Agentic AI (Olist Intelligent Marketplace)

Pós-graduação FIAP — Tech Challenge da disciplina de Agentic AI. Consultoria estratégica de IA para a
Olist, propondo agentes de IA orientados a negócio a partir de análise de dados.

## Estrutura do repositório

```
├── TECH CHALLENGE AGENTIC AI - FASE 1.pdf   # enunciado oficial do desafio
├── mapa_agentes_ia.qmd                      # relatório executivo (Quarto — fonte única)
├── mapa_agentes_ia.html / .pdf              # relatório renderizado
├── notebooks/
│   └── analise_exploratoria.ipynb           # análise exploratória do dataset Olist
├── styles/
│   ├── report.css                           # estilo da saída HTML (Arial 12, justificado)
│   └── preamble.tex                         # ajustes da saída PDF
└── dados/                                   # dataset bruto (NÃO versionado — ver abaixo)
```

## Dataset

Este projeto usa o **Brazilian E-Commerce Public Dataset by Olist** (~100 mil pedidos, 2016-2018).
A pasta `dados/` está no `.gitignore` por ser um dataset público grande (~120MB) e redownload
trivial. Para reproduzir a análise:

1. Baixe o dataset "Brazilian E-Commerce Public Dataset by Olist" no Kaggle.
2. Extraia os 9 arquivos CSV para a pasta `dados/` na raiz do projeto.
3. Os nomes esperados pelos notebooks são os nomes originais do Kaggle (ex.:
   `olist_orders_dataset.csv`, `olist_order_items_dataset.csv`, etc.).

## Como reproduzir

```bash
# Notebook de análise exploratória
jupyter nbconvert --to notebook --execute --inplace notebooks/analise_exploratoria.ipynb

# Relatório executivo (gera HTML e PDF)
quarto render mapa_agentes_ia.qmd --to html
quarto render mapa_agentes_ia.qmd --to pdf
```

Requer Python 3 com `pandas`, `numpy`, `matplotlib`, `scipy`, `jupyter`, além do
[Quarto CLI](https://quarto.org) e uma distribuição LaTeX (TinyTeX) para o PDF.

## Entregáveis da Fase 1

- [x] Relatório executivo com análises, agentes propostos, arquitetura conceitual e prompts
- [x] Mapa de agentes de IA (≥3 agentes)
- [ ] Arquitetura conceitual inicial
- [ ] Estruturação de prompts para os agentes
- [ ] Vídeo executivo (≤5 min)
