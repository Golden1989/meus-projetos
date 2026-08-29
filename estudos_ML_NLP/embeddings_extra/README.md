# Exercícios extras — Embeddings

Prática focada só em **embeddings**, além dos módulos do curso Intermediate NLP
(`../inter_to_NLP/`). Feito para reduzir a dificuldade de sintaxe antes de usar
esse processo — treinar embeddings e treinar um modelo em cima deles — no
projeto final de faculdade.

Mesma convenção do resto do repositório:

- **`exercicios_*.ipynb`** — exercício em branco, só com as instruções e as
  células de código vazias (marcador `# N.N`). Ficar em branco no repositório é
  o esperado.
- **`exercicios_*_solucoes.ipynb`** — gabarito resolvido e executado, com os
  outputs.

Tudo roda localmente no ambiente conda `ml` (`../../environment.yml`), sem
download: os dados de cada notebook são criados na própria célula. Os notebooks
3 e 4 reaproveitam a base de SMS spam/ham do Módulo 1.

## Notebooks

| Notebook | Tema | O que treina |
|---|---|---|
| `exercicios_1_nn_embedding_sintaxe` | A camada `nn.Embedding` | Criar, formatos de entrada/saída, `padding_idx`, `from_pretrained`, congelar/descongelar, média com máscara |
| `exercicios_2_cbow` | Word2Vec CBOW do zero | Gerar amostras contexto→alvo, `nn.Embedding` + média + `Linear`, loop de treino em PyTorch |
| `exercicios_3_classificador_com_embeddings` | Classificador com embedding treinável | Pipeline completo: vocabulário → índices com padding → `TensorDataset`/`DataLoader` → média com máscara → `Linear` → `BCEWithLogitsLoss` → avaliação |
| `exercicios_4_embeddings_pre_treinados` | Usar embeddings pré-treinados | Alinhar a matriz ao vocabulário do modelo, carregar com `from_pretrained`, congelado vs fine-tuning, similaridade/analogia |

Ordem sugerida: 1 → 2 → 3 → 4. O 1 é só sintaxe; o 3 é o que mais se parece com
o que o projeto final vai precisar.

## Arquivos gerados pelos gabaritos

Ao rodar os `_solucoes`, alguns notebooks salvam artefatos na pasta
(`cbow_embeddings.npy`, `cbow_vocab.json`, `aligned_matrix.npy`,
`aligned_vocab.json`) — são as matrizes de embedding + o vocabulário na mesma
ordem, que é o par que se carrega num modelo depois.
