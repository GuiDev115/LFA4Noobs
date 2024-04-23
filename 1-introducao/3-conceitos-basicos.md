# Definições 

Aqui teremos um pouco de Matemática Discreta, e o uso de conceito sobre conjunções matemáticas:

**Linguagem:** conjunto de palavras sobre um alfabeto 
**Alfabeto (Σ):** conjunto de símbolos de uma linguagem 
**Palavra (string):** sequência de símbolos de um alfabeto
**Σ*:** é o conjunto de todas as palavras geradas por Σ 
**A " * " (estrela):** operador de Kleene

### Se Σ = {a,b, c}, 

### então Σ* inclui: 
	- Tamanho zero: λ 
	- Tamanho um: a b c 
	- Tamanho dois: aa ab ac ba bb bc ca cb cc 
	- Tamanho três: aaa aab abb bbb baa bba bbb aac acc acb abc e etc
	- Tamanho mais até o infinito

**Tamanho de uma palavra w:** número de aplicações do passo recursivo para se obter w

**Linguagem (L):** subconjunto do conjunto de todas as possíveis palavras de um alfabeto (L ⊆ Σ* )

Palavras que interessam são as palavras *válidas* 
Exemplo: se Σ = {Maria, fala,alto}, quais são as palavras válidas?
e.g: `Maria Fala Alto`
`Maria Alto Fala`
`Alto Fala Maria`
# Recomendável Saber:

Aqui iremos aprofundar `BASTANTE` na matemática discreta, aproveito falar que a partir daqui, o requisito é sim saber o básico sobre, caso contrario: [**pule essa etapa.**](../2-linguagem-regulares/01-expressoes-regulares.md)
### Concatenação:
Seja u, v ∈ Σ* . A concatenação de u e v, escrita uv, é uma operação binária em Σ* definida assim: 

base: se tam(v) = 0, então v = λ e uv = u 

passo recursivo: se tam(v) = n, onde n > 0 então: 
v = wa, com tam(w) = n − 1 e a ∈ Σ 

Assim, uv = u(wa) = (uw)a 

- Concatenação `não` é comutativa

Prova: (por contra-exemplo) 
- Se u = ab e v = ca então uv = abca e vu = caab C

Concatenação é `associativa`: (uv)w = u(vw)

### Prova de Associatividade 
(por indução no comprimento da palavra w) 

Teorema: Seja u, v, w ∈ Σ* , então (uv)w = u(vw) 

#### Base: se tam(w) = 0, então w = λ 
- (uv)w = (uv)λ = uv `e` u(vw) = u(vλ) = u(v) = uv 
- Logo, `(uv)w = u(vw)`
#### Hipótese: (uv)w = u(vw) ∀w,tam(w) ≤ k 

#### Passo indutivo: provar (uv)w = u(vw) ∀w,tam(w) = k + 1 

- Seja w = xa, tam(x) = k, a ∈ Σ 

- (uv)w = (uv)(xa) = 
- = ((uv)x)a (definição concatenação) 
- = (u(vx))a (uso da hipótese de indução) 
- = u((vx)a) (definição concatenação) 
- = u(v(xa)) (definição concatenação) 
- = u(vw)****

Ir para: [2.1 Expressões Regulares](../2-linguagem-regulares/01-expressoes-regulares.md)