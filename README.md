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

`Sobre os Nomes de Chaves no Redis:`
- São únicos 
- Binários seguros
- Possuem limite de tamanho de até 512 megabytes 

! Qualquer sequência binária pode ser usada como chave <br>
! Chaves super longas não são recomendadas 

`Sobre Espaços de Chaves:`
- Todos as chaves ocupam o mesmo espaço
- Naõ existe uma separação automática das chaves em grupos ou coleções 
- Sempre padronizar os nomes das chaves

`Banco de Dados Lógico:`

- Idendtificado por uma base de index 0
- Dentro de um banco de dados os nomes das chaves são únicos, porém o mesmo nome de chave pode aparecer em bancos diferentes 
- Os bancos de dados lógicos fornecem separação de nomes de chaves 

`Exemplo: Como um nome de chave é construído:`
> * user:id:followers
>     * "user:1000:followers"
>        * user: Nome do Objeto
>        * 1000: Identifiação única
>        * followers: Objeto composto 
  
Os nomes de chaves diferenciam maiúsculas de minúsculas.

`Comandos Básicos:`

- SET: usamos esse comando para armazenar um valor em uma chave 
- GET: Retorna o valor da chave 
- KEYS, SCAN: São comandos usados para iterar obre todas as chaves de um banco de dados redis, ou para obter todas as chaves que atendem determinado padrão
    - OBS: Scan é mais indicado para o ambiente de Produção 
- DEL: Remove a chave e a memória associada a ela
- UNLINK: Desvincular uma chave, assim não haverá mais a memória vinculada a ela.
- EXIST: Verificar a existência da chave

### Praticando 
