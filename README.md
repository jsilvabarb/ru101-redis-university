# ru101-redis-university
 RU101 course class notes
 
 - [Semana-1](#Semana-1)
 - [Semana 2](#Semana-2)
 - [Semana 3](#Semana-3)
 - [Semana 4](#Semana-4)
 - [Semana 5](#Semana-5)
 - [Semana 6](#Semana-6)

## Semana-1
### Redis Structures 
- [Keys](#Keys)
- [Strings](#Keys)
- [Hashes](#Hashes)
- [Listas](#Listas)
- [Sets e SortedSets](#Sets)

## Keys 

Chaves são a principal maneira de acessar os valores de dados no Redis, a maioria dos comandos do Redis opera uma ou todas as chaves.

Sobre os Nomes de Chaves no Redis:
- São únicos 
- Binários seguros
- Possuem limite de tamanho de até 512 megabytes 

! Qualquer sequência binária pode ser usada como chave
! Chaves super longas não são recomendadas 
