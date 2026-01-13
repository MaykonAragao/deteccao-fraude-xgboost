# 💳 Detecção de Fraude em Cartão de Crédito com XGBoost

![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-brightgreen)

## 📄 Descrição do Projeto

Este projeto aborda o desafio crítico de **detecção de fraude em transações de cartão de crédito** utilizando Machine Learning. O foco principal foi construir um modelo de alta performance capaz de lidar com um **dataset extremamente desbalanceado**, onde as transações fraudulentas representam menos de 0.2% do total.

## 📊 Dataset

O dataset utilizado é um conjunto de dados anonimizados de transações de cartões de crédito ocorridas em setembro de 2013 por portadores de cartões europeus.

*   **Link para o Dataset:** [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

## 🛠️ Ferramentas e Técnicas Utilizadas

*   **Linguagem:** Python 3
*   **Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost.
*   **Técnicas Chave:**
    *   **Pré-processamento:** `StandardScaler` para dimensionar as features `Time` e `Amount`.
    *   **Validação:** Divisão de dados treino/teste **estratificada** para manter a proporção de classes.
    *   **Modelagem:** Utilização do `XGBClassifier`, um algoritmo de Gradient Boosting.
    *   **Tratamento de Desbalanceamento:** Aplicação do hiperparâmetro `scale_pos_weight` para dar mais importância à classe minoritária (fraudes).
    *   **Avaliação:** Análise aprofundada com `classification_report`, `ConfusionMatrixDisplay` e a **Curva Precision-Recall**.

## 📈 Resultados do Modelo

O modelo XGBoost treinado alcançou uma performance excepcional, ideal para um cenário de detecção de fraude:

*   🎯 **Recall de 79%:** O modelo foi capaz de identificar **79% de todas as transações fraudulentas reais**, minimizando as perdas financeiras.
*   🛡️ **Precisão de 88%:** De todas as transações sinalizadas como fraude, **88% eram de fato fraudulentas**, garantindo uma baixa taxa de "alarmes falsos" e otimizando o trabalho da equipe de análise.
*   **AUC da Curva P-R:** A Área Sob a Curva Precision-Recall foi de **0.83**, confirmando a robustez e o excelente poder de discriminação do modelo.

## 🚀 Como Executar o Projeto

1.  Clone este repositório.
2.  Instale as dependências (`pip install pandas numpy matplotlib seaborn scikit-learn xgboost`).
3.  Execute o notebook `analise_fraude_cartao.ipynb` em um ambiente Jupyter.
