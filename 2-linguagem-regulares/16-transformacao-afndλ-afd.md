# WIP
### AFND-λ → AFND

- i.e., δND−λ → δND
- Importante: AFND pode ter mais de um estado inicial

### AFND → AFD
- i.e., δND → δD
- Importante: Dado um AFND com n estados, o AFD correspondente pode ter até 2n estados (e.g., 5 → 32)
	- Por isso, abordaremos um algoritmo de construção de estados sob demanda (para evitar estados inúteis)
- Caso não haja transições λ, pular passo (1)

Ir para: [2.16 Exemplo de Transformação AFND λ para AFD](17-exemplo-transformacao.md)
