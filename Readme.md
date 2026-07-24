# 📊 Detecção de Anomalias em Transações Bancárias com Python

Pipeline de Machine Learning completo e de ponta a ponta (*end-to-end*) desenvolvido para identificar fraudes e anomalias em transações financeiras utilizando algoritmos de classificação avançados e interpretabilidade de modelos.

---

## 📋 1. Sobre o Contexto e Desafio

* **Cenário do Problema:** 
  * Transações financeiras fraudulentas representam uma parcela mínima do volume total de dados.
  * Ocorre um forte cenário de **classificação altamente desbalanceada**, fazendo com que modelos convencionais ignorem a classe minoritária.
* **Abordagem da Solução:**
  * Aplicação de técnicas avançadas de engenharia de atributos.
  * Estratégias robustas de balanceamento de dados e modelagem preditiva.
  * Foco em alta sensibilidade (*recall*) para detecção eficiente de fraudes.

---

## 🛠️ 2. Tecnologias e Ferramentas Utilizadas

* **Linguagem Principal:** 
  * Python
* **Manipulação e Análise de Dados:** 
  * Pandas, NumPy
* **Machine Learning & Balanceamento:** 
  * Scikit-Learn, Imbalanced-Learn (SMOTE), XGBoost
* **Métricas e Validação:** 
  * ROC-AUC, Precision-Recall Curve, Classification Report, GridSearchCV
* **Explicabilidade (XAI):** 
  * SHAP (Shapley Additive exPlanations)
* **Ambiente de Desenvolvimento:** 
  * Google Colab / Jupyter Notebook

---

## ⚙️ 3. Etapas do Pipeline Desenvolvido

* **Análise Exploratória:** 
  * Diagnóstico estatístico inicial do desbalanceamento severo na variável alvo (`Class`).
* **Feature Engineering:** 
  * Transformação logarítmica (`Amount_log`) para suavizar a assimetria dos valores monetários.
  * Padronização robusta utilizando `StandardScaler`.
* **Modelagem Baseline:** 
  * Implementação de Regressão Logística como linha de base estatística.
  * Avaliação detalhada por curvas ROC e Precision-Recall.
* **Tratamento de Desbalanceamento:** 
  * Testes comparativos aplicados via *Undersampling*, *Oversampling* (SMOTE) e pesos de classes ajustados (`class_weight` / `scale_pos_weight`).
* **Modelagem Avançada:** 
  * Treinamento com Random Forest e XGBoost.
  * Otimização de hiperparâmetros via `GridSearchCV` focado em *Recall* e ajuste de limiar de decisão (*threshold* customizado para `0.3`).
* **Explicabilidade (XAI):** 
  * Aplicação prática do SHAP para decodificar o impacto e a importância individual das variáveis nas predições do XGBoost.

---

## 📈 4. Principais Resultados e Conclusão

* **Eficiência dos Modelos:** 
  * Algoritmos de *Gradient Boosting* (como o XGBoost) aliados a estratégias adequadas de penalização de classes provaram ser altamente eficazes na mitigação de falsos negativos.
* **Valor Corporativo:** 
  * A integração com o **SHAP** eleva a solução ao padrão corporativo, fornecendo total transparência e interpretabilidade sobre os fatores de risco avaliados pelo modelo.

---

## 🚀 5. Como Executar o Projeto

* **Passo a Passo:**
  1. Clone o repositório ou faça o download direto do arquivo `.ipynb`.
  2. Abra o arquivo no [Google Colab](https://colab.research.google.com/) ou em seu ambiente Jupyter Notebook local.
  3. Execute as células de forma sequencial. O conjunto de dados público de transações de cartão de crédito será baixado automaticamente através da URL oficial.
