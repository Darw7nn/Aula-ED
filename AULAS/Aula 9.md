# Resumo dos Notebooks de Grafos

## Visão Geral

Ambos os notebooks exploram a construção e visualização de **grafos não-direcionados** usando as bibliotecas Python `networkx` e `matplotlib`. O objetivo principal é representar relações entre pessoas (nós) por meio de arestas, e então visualizar o grafo resultante.

---

## Notebook 1 — `Grafo_AULA_9.ipynb`

### Contexto
Notebook de aula com um grafo de rede social fictícia entre 10 personagens.

### Nós (Pessoas)
`Harry`, `Gayle`, `Frank`, `Emily`, `Dave`, `Cathy`, `Bill`, `Jeff`, `Audrey`, `Llana`

### Arestas (Conexões)
15 conexões no total, incluindo:
- Gayle ↔ Bill, Audrey, Cathy
- Audrey ↔ Bill, Llana
- Llana ↔ Harry, Dave
- Harry ↔ Jeff
- Emily ↔ Frank, Jeff, Cathy, Bill, Dave
- Frank ↔ Dave

### O que foi feito
1. **Criação do grafo** com `nx.Graph()` e adição de nós e arestas manualmente.
2. **Inspeção do grafo**: exibição dos nós, arestas, quantidade de nós (10) e arestas (15).
3. **Visualização**: layout `spring_layout` com seed fixada (`seed=42`), nós em azul claro com rótulos em negrito.

---

## Notebook 2 — `grafos.ipynb`

### Contexto
Notebook de prática própria com um grafo de rede social em português, com 7 pessoas.

### Nós (Pessoas)
`João`, `Paulo`, `Maria`, `Joana`, `Antonia`, `Lili`, `Raimundo`

> ⚠️ Observação: `Raimundo` foi adicionado como nó, mas **não possui nenhuma aresta** — é um nó isolado no grafo.

### Arestas (Conexões)
8 conexões no total:
- João ↔ Paulo
- Paulo ↔ Maria, Joana, Antonia, Lili
- Maria ↔ Joana
- Joana ↔ Antonia
- Antonia ↔ Lili

### O que foi feito
1. **Criação do grafo** seguindo a mesma estrutura do notebook de aula.
2. **Inspeção do grafo**: exibição dos nós, arestas e suas contagens.
3. **Visualização**: mesmo estilo do notebook anterior — `spring_layout`, nós azuis, rótulos em negrito, título "Representação em Grafo simples".

---

## Conceitos Aplicados

| Conceito | Descrição |
|---|---|
| **Grafo não-direcionado** | Conexões sem direção definida (A ↔ B) |
| **Nó (vértice)** | Representa uma entidade (pessoa) |
| **Aresta** | Representa uma relação entre duas entidades |
| **Nó isolado** | Nó sem nenhuma aresta (ex: Raimundo) |
| **spring_layout** | Algoritmo de posicionamento baseado em forças físicas |

## Bibliotecas Utilizadas
- **`networkx`** — criação, manipulação e análise de grafos
- **`matplotlib`** — visualização gráfica dos grafos
