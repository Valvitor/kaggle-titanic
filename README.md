<h1 align="center">🛳️ Kaggle Challenge: Titanic - Machine Learning from Disaster</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Status" />
  <img src="https://img.shields.io/badge/Language-Python-blue?style=for-the-badge&logo=python" alt="Language" />
  <img src="https://img.shields.io/badge/Model-XGBoost-orange?style=for-the-badge" alt="Model" />
</p>

## 📌 Visão Geral do Projeto
Este repositório contém a solução e a documentação investigativa para a famigerada competição do **Titanic** no Kaggle. O objetivo deste laboratório foi prever a sobrevivência de passageiros combinando técnicas avançadas de *Feature Engineering* espacial e imputação multivariada.

---

## 🏗️ Modelagem e Resultados

Para mapear e extrair o máximo das distribuições estatísticas desse naufrágio e atingir métricas de elite, dividimos o projeto em duas fases de exploração contínuas.

### V1: O Baseline Sólido (`exploration.ipynb`)
Um modelo de fundação focado em validar as premissas sociais primárias (A regra *Women and Children First* e distinção de Classes).
*   **Tratamentos:** Extração simples de "Títulos" nos nomes via Expressões Regulares (`Regex`) e Imputação Numérica usando medianas grupais.
*   **Modelo:** `RandomForestClassifier`
*   **Validação (Local CrossVal):** `82.12%`

### V2: Avançado / Ouro (`02_advanced_exploration.ipynb`)
Modelo otimizado para atacar o real "teto de vidro" imposto pela natureza errática e barulhenta de um desastre físico.
*   **Feature Engineering Topológica:** Mapeamento do deck geométrico de embarque (extraindo a primeira letra obscura de `Cabin`) para rastrear o posicionamento do passageiro em relação aos botes.
*   **Feature Engineering Espacial:** Junção comportamental criando um peso de `Ticket Frequency`, provando se o passageiro morreu abraçado ao seu grupo/família.
*   **Imputação Tridimensional Otimizada:** Substituição da métrica de Medianas por um algoritmo `KNNImputer` que rastreia os 5 passageiros "mais geneticamente puros" por proximidade n-dimensional para prever a exata idade não documentada no manifesto de passageiros.
*   **O Algoritmo Mestre:** `Extreme Gradient Boosting (XGBoost)` tunado para prevenir sobreajuste (*early_stopping*).
*   **Score Final:** *(Insira aqui o seu Score Público do Leaderboard que saiu nessa segunda versão! Ex: 78%+)*.
*   **Validação (CrossVal k=5):** `82.72%`

---

## 🛠️ Stack de Ferramentas Utilizadas

*   **Manipulação de Dados:** `Pandas`, `Numpy`
*   **Machine Learning Base:** `Scikit-learn` (KNN Imputer, Ensembling, Pipelines)
*   **Gradient Boosting:** `XGBoost`
*   **Data Visualization:** `Matplotlib`, `Seaborn`

---

## 📂 Como Rodar este Projeto Localmente

1. Clone este repositório.
2. Certifique-se de baixar a pasta local `data/` pelo Kaggle API na base deste diretório (A pasta de dados é pesada e não se encontra neste repositório por estar blindada via GitIgnore).
3. Instale as dependências executando:
   ```bash
   pip install -r requirements.txt
   ```
4. Navegue até a pasta `notebooks/` e execute as células dos laboratórios jupyter na ordem cronológica.

---
> Elaborado por **Valvitor Santos** para portfólio documentado do ecosistema e desafios do Kaggle.
