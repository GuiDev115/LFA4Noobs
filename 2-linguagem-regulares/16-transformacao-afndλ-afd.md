# Transformação AFND-λ → AFD

A transformação é feita em dois passos:

## Passo 1: AFND-λ → AFND

- i.e., δND−λ → δND
- **Importante:** O AFND resultante pode ter **mais de um estado inicial**
- Caso não haja transições λ, **pular este passo**

### Fecho-λ (fecho-lambda)

O fecho-λ de um estado qi, escrito **fecho−λ(qi)**, é o conjunto formado por qi mais todos os estados acessíveis a partir de qi lendo apenas transições λ:

> fecho−λ(qi) = { qi } ∪ { qj | qi →(λ)→* qj }

### Algoritmo δND−λ → δND

**Estados iniciais do AFND:**
- São todos os estados de **fecho−λ(q0)**
- Todos esses estados são iniciais no AFND resultante

**Para cada estado qi e cada símbolo a ∈ Σ:**
1. Considere todos os estados em fecho−λ(qi)
2. A partir de cada um desses estados, consume o símbolo `a` pelo δND−λ, chegando a um conjunto de estados
3. Para cada estado qj atingido, adicione **fecho−λ(qj)** ao resultado

Formalmente:
> δND(qi, a) = ∪ { fecho−λ(qj) | qj ∈ δND−λ(q, a), q ∈ fecho−λ(qi) }

---

## Passo 2: AFND → AFD

- i.e., δND → δD
- **Importante:** Dado um AFND com n estados, o AFD correspondente pode ter até **2ⁿ estados** (e.g., 5 estados → até 32 estados)
- Para evitar estados inúteis, utiliza-se um **algoritmo de construção sob demanda**

### Algoritmo δND → δD (Construção de Subconjuntos)

O AFD resultante tem como estados **conjuntos de estados** do AFND:

1. O estado inicial do AFD é o conjunto dos estados iniciais do AFND
2. Para cada estado S (conjunto de estados) e símbolo a ∈ Σ:
   > δD(S, a) = ∪ { δND(qi, a) | qi ∈ S }
3. Um estado S é **final** no AFD se S ∩ F ≠ ∅ (i.e., se algum estado do conjunto era final no AFND)
4. Adicionar à fila apenas os novos estados ainda não visitados (construção sob demanda)

Ir para: [2.17 Exemplo de Transformação AFND-λ para AFD](17-exemplo-transformacao.md)
