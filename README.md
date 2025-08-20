# Previsão de Churn de Clientes - Análise de Dados e Modelagem Preditiva
**Missão:** Desenvolver modelos preditivos capazes de prever quais clientes têm maior chance de cancelar seus serviços.

## Objetivos do Projeto 
- Preparar os dados para a modelagem (tratamento, encoding, normalização).  
- Realizar análise de correlação e seleção de variáveis.  
- Treinar dois ou mais modelos de classificação.  
- Avaliar o desempenho dos modelos com métricas.  
- Interpretar os resultados, incluindo a importância das variáveis.  
- Criar uma conclusão estratégica apontando os principais fatores que influenciam a evasão.

## O que será praticado
✅ Pré-processamento de dados para Machine Learning  
✅ Construção e avaliação de modelos preditivos  
✅ Interpretação dos resultados e entrega de insights  
✅ Comunicação técnica com foco estratégico

## Ferramentas, Linguagens e Bibliotecas
- Google Colab  
- Python  
- Pandas  
- Numpy  
- Scikit-learn  
- Matplotlib  
- Seaborn  

---

## ⚙️ Preparação dos Dados
### 🛠️ Etapas de tratamento dos dados
- **Normalização e Padronização:** variáveis numéricas foram padronizadas para treinar modelos sensíveis a escala, como KNN.  
- **Codificação de variáveis categóricas:** variáveis não numéricas foram transformadas via OneHotEncoder.  
- **Balanceamento das classes:** a evasão (churn) é uma classe minoritária; foi aplicada apenas no conjunto de treino.  
- **Separação dos dados:**
  - Treino e teste com proporção 70/30.
  - Foi realizado o balancemento utilizando o método SMOTE no treino pois modelos treinados em datasets desbalanceados tendem a ser enviesados para a classe majoritária, o que significa que eles podem ter uma alta acurácia geral (por acertarem a maioria dos casos da classe majoritária), mas podem ter um desempenho ruim na identificação da classe minoritária (os clientes que evadiram), que é a classe de maior interesse para este problema.

---

## 📊 Análise Exploratória (EDA)
- Foram avaliadas distribuições de variáveis, correlações entre features e relações com churn.  
- Identificação de padrões que poderiam influenciar a evasão, como comportamento de compra, uso de serviços e variáveis demográficas.  
- Visualizações foram usadas para destacar insights iniciais, como concentração de churn em determinados perfis.
<img width="850" height="547" alt="dispercao1" src="https://github.com/user-attachments/assets/7ddde7cc-755e-44d9-9937-4d0b14ea584e" />
<img width="850" height="547" alt="dispercao2" src="https://github.com/user-attachments/assets/5ac69efa-d1f0-4364-8bec-dfa1031da816" />

---

## Modelagem e Avaliação
### Modelos aplicados:
- **Regressão Logística**  
- **Árvore de Decisão Otimizada**  
- **KNN Otimizado**  
- **Random Forest Otimizado**  

### Métricas utilizadas:
- Acurácia  
- Precisão  
- Recall  
- F1-score  
- AUC-ROC  
- Matriz de Confusão
<img width="1920" height="826" alt="Colagem 3" src="https://github.com/user-attachments/assets/e57b48cb-a622-4492-b0ed-c6a9445dcca7" />
<img width="1920" height="781" alt="Colagem 1" src="https://github.com/user-attachments/assets/21a40ff1-7867-41ab-b310-d6f0297245d4" />
<img width="1920" height="829" alt="Colagem 2" src="https://github.com/user-attachments/assets/800c1555-1495-40d8-9956-e1f98dbda943" />

**Resumo do desempenho dos modelos:**

| Modelo | Acurácia | Precisão | Recall | F1-Score | AUC-ROC |
|--------|----------|----------|--------|----------|---------|
| Regressão Logística | 0.266 | 0.266 | 1.0 | 0.420 | 0.434 |
| Árvore de Decisão Otimizada | 0.746 | 0.523 | 0.510 | 0.516 | 0.695 |
| KNN Otimizado | 0.739 | 0.512 | 0.342 | 0.410 | 0.718 |
| Random Forest Otimizado | 0.771 | 0.557 | 0.679 | 0.612 | 0.820 |

### Justificativas para decisões:
- Random Forest foi escolhido como modelo principal por apresentar **melhor desempenho geral**, com maior F1-score, AUC-ROC e equilíbrio entre precisão e recall.  
- KNN e Árvore de Decisão foram utilizados para comparação e análise de robustez dos modelos.
---

## 💡 Análise de Importância das Variáveis
- A partir do Random Forest otimizado, foram identificadas as **variáveis mais relevantes para prever churn**.  
- As **top 5 variáveis** destacadas foram analisadas, permitindo priorizar ações estratégicas.  
- Visualizações em gráfico de barras auxiliaram a interpretação do impacto de cada variável na previsão.
<img width="790" height="590" alt="Variáveis Top 5 Random Forest" src="https://github.com/user-attachments/assets/028fadbf-1c55-42c4-90b9-b395370753b7" />

---

## 💡 Estratégias de Retenção Propostas
- Foco em clientes identificados como de alto risco pelo modelo.  
- Ações específicas podem ser desenhadas considerando as **top variáveis que mais influenciam o churn**, como ajustes em serviços, comunicação ou ofertas personalizadas.  
- Monitoramento contínuo do comportamento de clientes para validar e ajustar o modelo.

---

## 📦 Requisitos
- Python 3.x  
- Bibliotecas: Pandas, Numpy, Scikit-learn, Matplotlib, Seaborn  
- Dados de clientes com histórico de uso de serviços e informações demográficas  
