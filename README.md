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

## 🛠️ Tecnologias Utilizadas
* **Python**
* **Pandas** (Tratamento, limpeza e diagnóstico estatístico dos dados)
* **Google Colab** (Ambiente de desenvolvimento)

---
*Nota: Este repositório foi desenvolvido para fins de demonstração de portfólio em análise de dados e estatística aplicada.*
