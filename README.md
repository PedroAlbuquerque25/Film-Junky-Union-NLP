# 🎬 Film Junky Union - Sentiment Analysis (NLP)

Este repositório contém o desenvolvimento de um modelo de Processamento de Linguagem Natural (NLP) para a **Film Junky Union**. O objetivo foi criar um sistema capaz de filtrar e categorizar automaticamente resenhas de filmes, detectando críticas negativas com alta precisão.

## 🎯 Objetivo do Projeto
Treinar um modelo de classificação binária para identificar o sentimento de resenhas do IMDB, atingindo a meta de desempenho de uma métrica **F1-score de pelo menos 0,85**.

## 🛠️ Stack Técnica
- **Linguagem:** Python
- **Processamento de Texto:** `spaCy` (Lematização), `NLTK` (Stopwords), `Regular Expressions (re)`.
- **Vetorização:** `TF-IDF` (Term Frequency-Inverse Document Frequency).
- **Modelos:** `LightGBM` (LGBMClassifier) e `Logistic Regression`.
- **Ambiente:** Conda / VS Code.



## 📊 Performance do Modelo Final (LightGBM + TF-IDF)

O modelo final utilizando **LightGBM** treinado sobre representações TF-IDF processadas via spaCy superou as expectativas iniciais:

| Métrica | Resultado (Teste) |
| :--- | :--- |
| **F1-Score** | **0.88** |
| **Acurácia** | **0.88** |
| **ROC AUC** | **0.95** |

### Principais Insights
* **Eficiência:** O uso de TF-IDF com modelos de árvores de decisão (LightGBM) provou ser uma solução de excelente custo-benefício, evitando a necessidade de modelos pesados de Deep Learning (como BERT).
* **Consistência:** O modelo apresentou uma generalização sólida (F1 0.97 no treino vs 0.88 no teste), mantendo-se estável para dados textuais extensos.
* **Linguística:** A lematização via spaCy foi crucial para reduzir a dimensionalidade do vocabulário e focar no núcleo semântico das críticas.



## 📂 Estrutura do Repositório
- `notebooks/`: Jupyter Notebook com toda a análise, pré-processamento e treinamento.
- `data/`: Local para armazenamento do dataset (IMDB reviews).
- `.gitignore`: Configurado para ignorar ambientes virtuais e arquivos de dados pesados.

## 🚀 Próximos Passos
- Implementar redução de dimensionalidade com **SVD (LSA)**.
- Testar modelos híbridos combinando LightGBM com embeddings densos (fastText).
- Validar o modelo em cenários de produção com dados em tempo real.

---

**Desenvolvido por [Pedro Albuquerque]**

---

## 🤝 Contact
[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/phaa/)