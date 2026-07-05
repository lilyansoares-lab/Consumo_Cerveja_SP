# Análise Preditiva de Demanda: Consumo de Cerveja em São Paulo 🍺

Este repositório contém um estudo focado em modelagem estatística para previsão de demanda, aplicando técnicas de **Regressão Linear Simples e Múltipla**. O objetivo principal é transformar dados climáticos e de calendário em insights acionáveis para otimização de estoque e planejamento logístico.

---

## 💼 Contexto de Negócio
A previsão de demanda é essencial para evitar o desabastecimento em períodos de pico e reduzir custos com excesso de mercadoria parada. Utilizando dados históricos de consumo na região de São Paulo, este projeto analisa como fatores climáticos (temperatura e pluviosidade) combinados com o efeito calendário (finais de semana) impactam o comportamento do consumidor.

---

## 📊 Estrutura dos Dados e Diagnóstico
A base de dados traz registros diários contendo:
* **Temperatura Máxima (°C)**: Utilizada como principal preditor de calor.
* **Chuva (mm)**: Indicador de precipitação, essencial para analisar a retração de consumo.
* **Final de Semana**: Variável binária (1 para sábado/domingo, 0 para dias úteis).
* **Consumo (Litros)**: A variável alvo (*target*) do modelo.

O diagnóstico inicial dos dados revelou uma alta amplitude térmica (temperaturas máximas variando entre 15°C e 36°C) e uma volatilidade intermitente no volume de chuva (com desvio padrão de 12.41 mm e picos de até 94.8 mm), fatores que justificam a abordagem por regressão múltipla para isolar esses efeitos.

---

## 🧠 Abordagem Estatística
O código está estruturado em duas etapas principais de modelagem:
1. **Regressão Linear Simples**: Focada exclusivamente no impacto isolado da Temperatura Máxima sobre o consumo.
2. **Regressão Linear Múltipla**: Análise conjunta do clima (Temperatura Máxima e Chuva) e da sazonalidade semanal (Finais de Semana) para uma previsão mais robusta.

---

## 🎯 Conclusão e Visão Estratégica

A modelagem estatística demonstrou resultados sólidos e aplicabilidade direta na tomada de decisão:

* **Poder Explicativo Alto**: O modelo de **Regressão Linear Múltipla alcançou um $R^2$ de 72,3%**, o que significa que mais de 72% da variação diária no consumo de cerveja é explicada conjuntamente pela temperatura máxima, pela ocorrência de chuva e pelo efeito de ser final de semana. Isso reduz drasticamente a incerteza operacional e o risco de erro pela metade em relação ao modelo simples.
* **Estratégia de Curto Prazo (Até 15 dias - Operacional)**: Utilizar a previsão do tempo real (Temperatura Máxima + Probabilidade de Chuva). Como o horizonte é curto e a assertividade meteorológica é maior, permite o ajuste preciso do estoque de segurança e o acionamento de cargas extras/motoristas parceiros para os Finais de Semana.
* **Estratégia de Longo Prazo (Acima de 15 dias - Estratégico)**: Utilizar a "média" histórica de temperatura e o calendário de feriados/finais de semana. Garante o planejamento de capacidade junto a fornecedores e grandes centros de distribuição para manter o estoque base de 6.432 litros, com reforços planejados para os meses de maior sazonalidade.

---

## 🛠️ Tecnologias Utilizadas
* **Python**: Linguagem base para todo o desenvolvimento do script.
* **Pandas**: Utilizado para a manipulação, limpeza, tratamento e diagnóstico estatístico descritivo da base de dados.
* **Scikit-Learn / Statsmodels**: Modelagem estatística para a criação, treinamento e avaliação dos modelos de Regressão Linear Simples e Múltipla (análise de coeficientes, R² e redução de incertezas).
* **Matplotlib / Seaborn**: Criação de gráficos e visualização de dados.
* **Google Colab**: Ambiente de desenvolvimento em nuvem utilizado para a construção e renderização do notebook.

---
*Nota: Este repositório foi desenvolvido para fins de demonstração de portfólio em análise de dados e estatística aplicada.*
