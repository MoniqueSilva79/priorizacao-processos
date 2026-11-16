# 🧭 Priorização de Processos para Automação com IA

**🔗 Demo ao vivo: https://moniquesilva79.github.io/priorizacao-processos/**

Pontua processos candidatos por **valor** (reais em jogo) e **facilidade de automação** (regras claras, dados digitais e exceções) e os posiciona em uma matriz: **quick wins, grandes apostas, complementares e evitar por ora**. Processos de alto risco recebem a marca de que exigem revisão humana.

## 🎯 Problema que resolve
Em todo programa de automação surge a mesma dúvida: por onde começar? Começar pelo processo mais visível, e não pelo de maior retorno e menor esforço, é a causa mais comum de projetos de IA que não saem do piloto. Esta matriz dá um critério objetivo e transparente para a conversa com as áreas de negócio.

## ✨ Funcionalidades
- Lista editável de processos com volume, tempo, % de regras claras, dados digitais, exceções e risco
- Potencial em R$/mês com custo da hora e parcela automatizável configuráveis
- Notas de valor e facilidade de 0 a 100 e prioridade combinada
- Matriz 2×2 com bolhas proporcionais ao valor e ranking numerado
- Alerta de revisão humana para processos de risco 4 ou 5
- Exemplo pronto com 7 processos típicos de backoffice e atendimento

## 🧮 Como o cálculo funciona
```
potencial (R$/mês) = volume × minutos ÷ 60 × custo da hora × parcela automatizável
valor              = potencial ÷ maior potencial da lista × 100
facilidade         = 100 × (0,4 × regras claras + 0,3 × (dados − 1) ÷ 4 + 0,3 × (5 − exceções) ÷ 4)
prioridade         = 0,6 × valor + 0,4 × facilidade
quadrante          = valor ≥ 50 e facilidade ≥ 50 → quick win, e assim por diante
```

## 📊 Exemplo (valores padrão)
| Indicador | Valor |
|---|---|
| 1º | Segunda via de fatura: quick win, prioridade 97 |
| 2º | Conciliação bancária: quick win, prioridade 89 |
| 3º | Triagem de e-mails do SAC: quick win, prioridade 86 |
| 5º | Onboarding de cliente PJ: grande aposta, exige revisão humana |
| 7º | Análise de contratos: evitar por ora, exige revisão humana |

## 🧰 Tecnologias
HTML, CSS e JavaScript puros, sem frameworks, sem dependências e sem servidor. Publicado no GitHub Pages.

## 🚀 Como rodar localmente
```bash
git clone https://github.com/MoniqueSilva79/priorizacao-processos.git
cd priorizacao-processos
python -m http.server 8000   # e acesse http://localhost:8000
```

## ⚠️ Limitações
Os pesos são um ponto de partida e podem ser ajustados no código para a realidade de cada empresa. O valor é relativo à lista: compare processos do mesmo portfólio.

## 🗺️ Próximos passos
- [ ] Pesos configuráveis na interface
- [ ] Importar e exportar a lista em CSV
- [ ] Estimativa de esforço em semanas

## 🔗 Série de calculadoras de IA
[Custo por tarefa de agentes](https://moniquesilva79.github.io/custo-agentes-ia/) · [Precificação do FTE digital](https://moniquesilva79.github.io/precificacao-fte-digital/) · [ROI e payback](https://moniquesilva79.github.io/roi-automacao-ia/) · [Priorização de processos](https://moniquesilva79.github.io/priorizacao-processos/) · [Revisão humana x custo do erro](https://moniquesilva79.github.io/revisao-humana-ia/) · [Curva de melhoria contínua](https://moniquesilva79.github.io/curva-melhoria-ia/)

---
Projeto autoral de **Monique da Silva Cruz**: [LinkedIn](https://www.linkedin.com/in/moniquesilva-cloud-ti-projetos-latam) · [outros projetos](https://github.com/MoniqueSilva79)
