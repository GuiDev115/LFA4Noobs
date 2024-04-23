# Gramática Regular (GR)

Uma GR é uma quádrupla (V, Σ, P, S): 

V = conjunto de símbolos não-terminais (variáveis) 
Σ = conjunto de símbolos terminais (Σ ∩ V = ϕ) 
P = conj. de regras (produções) 
S = símbolo não-terminal inicial (S ∈ V) 

### Regras:  µ → ν 

- µ ∈ V  (i.e., µ é um elemento de V) 
- ν ∈ λ | Σ | ΣV

### Exemplo 

L = palavras sobre {a,b} que começam e terminam com a e possuem pelo menos um b

GR(L): 
- S → aA 
- A → aA | bB 
- B → aB | bB | a

### Propriedade interessante de gramáticas regulares: 

Uma forma sentencial possui no máximo uma variável 
- sempre o símbolo mais à direita 

Toda aplicação de regra adiciona um terminal na palavra que está sendo derivada 
- exceto regra da forma A → λ

Ir para: [2.5 Exercícios](05-exercicios-GR.md)

Ir para: [2.7 Autômatos Determinísticos](07-automatos-deterministicos.md)