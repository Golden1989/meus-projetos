# Estudos de ML / NLP

Notebooks de prática feitos em paralelo aos cursos do [Kaggle Learn](https://www.kaggle.com/learn) (Pandas, Intro to Machine Learning, Intro to NLP, Intermediate NLP), rodando localmente em um ambiente conda (`ml`), sem dependência de internet ou download de datasets externos — os dados usados em cada módulo são criados no próprio notebook.

## Como cada pasta funciona

Cada módulo/curso tem dois notebooks para o mesmo tema:

- **`exercicios_*.ipynb`** — o exercício em branco, com as instruções e células de código vazias. É o template para praticar; **ficar em branco no repositório é o comportamento esperado**, não é um upload incompleto.
- **`exercicios_*_solucoes.ipynb`** — o gabarito, com o código já resolvido e executado (inclui os outputs).

A ideia é sempre tentar resolver o exercício em branco antes de olhar o gabarito correspondente.

## Estrutura

| Pasta | Curso | Módulos |
|---|---|---|
| `pandas/` | [Pandas](https://www.kaggle.com/learn/pandas) | um único notebook cobrindo o curso |
| `intro_to_machine_learning/` | [Intro to Machine Learning](https://www.kaggle.com/learn/intro-to-machine-learning) | um único notebook cobrindo o curso |
| `intro_to_NLP/` | [Intro to NLP](https://www.kaggle.com/learn-guide/intro-nlp) | 1. Cleaning Text Data · 2. Feature Extraction · 3. Modeling with XGBoost · 4. Evaluating NLP Models |
| `inter_to_NLP/` | [Intermediate NLP](https://www.kaggle.com/learn-guide/intermediate-nlp) | 1. Word Embeddings · 2. Preparing Text Data · 3. Recurrent Neural Networks · 4. LSTM · 5. Bidirectional LSTM |

Os módulos de `intro_to_NLP/` e `inter_to_NLP/` são interligados: cada um salva arquivos (`.csv`, `.npy`, `.json`) que o próximo carrega, formando um pipeline completo de classificação de SMS spam/ham.
