# Autômato Finito Não-Determinístico com Transições-λ

### Um AFND-λ é uma quíntupla (Q, Σ, δND−λ,q0, F): 

Q = conjunto finito de estados 
Σ = alfabeto 
δND−λ : Q x (Σ ∪ {λ}) → P(Q) = f. de transições de estados 
qo ∈ Q = estado inicial 
F ⊆ Q = conjunto de estados finais (aceitação)

Para todo AFND-λ, existe um AFND e um AFD equivalentes 
	i.e., não aumenta o poder computacional 
	
É muito similar ao AFND Tem como vantagem facilitar construções e demonstrações Por exemplo, o algoritmo ER → AFND-λ

### Conclusão

A diferença gritante do **AFND** para a **transição λ**, é apenas a inclusão do **"λ"** no autômato, isto é, o percurso *"vai"* para outro estado sem "escrever" ou "ler" algo, ele apenas muda de estado sem ler ou escrever algo do alfabeto presente da linguagem.

Isso é muito útil para conseguir transformar uma expressão regular para um autômato muito mais fácil, que no caso, será usado o **algoritmo de Thopson**, que veremos mais a frente. Com ele, podemos transformar uma ER em um autômato de forma automática.


L = {a k | k é múltiplo de 2 ou 3}

![](images/nurmeo-par-3-de-a.jpg)


Ir para: [2.14 Exercicios de AFND-λ](14-exercicio-afnd-λ.md)