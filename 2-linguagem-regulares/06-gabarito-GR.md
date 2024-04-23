1. L = a⁺ b* 

	S -> aA
	A -> aA | bB | λ
	B -> bB | λ

2. L = {λ} ∪ {ab}{ab}* {a}* 

	S -> aA | λ
	A -> bS | bB
	B -> aB | λ

3. L = palavras sobre {a,b, c} que todo b seja seguido de a 

	S -> aS | cS | bA | λ
	A -> aS

4. L = palavras sobre {a,b} com número par de a

	S -> bS | aA | λ
	A -> bA | aS

Ir para: [2.7 Autômatos Determinísticos](07-automatos-deterministicos.md)