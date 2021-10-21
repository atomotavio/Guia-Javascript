# Sintaxe e tipos

Além do java, a sintaxe de Javascript é baseada em AWk, Perl e Python. É uma linguagem case-sensitive.
Apesar de nao ser obrigatório, recomenda-se o uso de (;) ao final das declarações.

## Comentários

~~~javascript
// comentário de uma linha

/* isto é um comentário longo
   de múltiplas linhas.
 */
~~~

## Declarações

Existem 3 tipos de declaração em Javascript:

* Var = declara uma variável, opcionalmente, inicializando-a com um valor.
* Let = declara uma variável local de escopo do bloco.
* Const = declara uma constante de escopo de bloco, apenas de leitura.

### Variáveis

Nomes de variáveis, ou também, seus identificadores, devem obedecer determinadas regras. Ele deve começar com uma letra, underline ou cifrão. 

**LEMBRE-SE QUE JAVASCRIPT É SENSITIVE-CASE**

## Estrutura de dados e tipos

Tipos de dados:

Atualmente o javascript conta com seis tipos de dados primitivos:


* Boolean: true e false
* null:  Uma palavra-chave que indica valor nulo. Devido JavaScript ser case-sensitive, null não é o mesmo que Null, NULL, ou ainda outra variação
* undefined: Uma propriedade superior cujo valor é indefinido
* Number: 42 ou 3.14159
* String: "Howdy"
* Symbol: (novo em ECMAScript 6). Um tipo de dado cuja as instâncias são únicas e imutáveis
* Object

### Conversão de tipos de dados

Por javascript ser uma linguagem dinamicamente tipada voce nao precisa especificar o tipo de dado de uma variável quando declará-la.

#### Array literal

Um array literal é uma lista de zero ou mais expressões, onde cada uma delas representam um elemento do array, inseridas entre colchetes ([]). Quando você cria um array usando um array literal, ele é inicializado  com os valores especificados como seus elementos, e seu comprimento é definido com o  número de elementos especificados.