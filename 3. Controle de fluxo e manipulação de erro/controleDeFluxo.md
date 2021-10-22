
# Controle de fluxo

Declaração em bloco

{
  declaracao_1
  declaracao_2
  declaracao_3
}

Exemplo

~~~Javascript

while (x < 10) {
  x++;
}

~~~

**Importante**: Antes de ECMAScript 6 o JavaScript não possuía escopo de bloco. Variáveis introduzidas dentro de um bloco possuem como escopo a função ou o script em que o bloco está contido, e, definir tais variáveis tem efeito muito além do bloco em si. Em outras palavras, declarações de bloco não introduzem um escopo. Embora blocos "padrão" sejam uma sintaxe válida não utilize-os, em JavaScript, pensando que funcionam como em C ou Java porque eles não funcionam da maneira que você acredita. Por exemplo:

~~~Javascript

var x = 1;
{
  var x = 2;
}
console.log(x); // exibe 2

~~~

Este código exibe 2 porque a declaração var x dentro do bloco possui o mesmo escopo que a declaração var x antes do bloco. Em C ou Java, o código equivalente exibiria 1.

## Declarações condicionais

O javascript possui dois tipos de declaração condicional. A mais conhecida é o if, mas ele também possui a switch.

### IF

~~~Javascript

if (condicao) {
  declaracao_1;
} else {
  declaracao_2;
}

~~~

### SWITCH

~~~Javascript

switch (expressao) {
   case rotulo_1:
      declaracoes_1
      [break;]
   case rotulo_2:
      declaracoes_2
      [break;]
   ...
   default:
      declaracoes_padrao
      [break;]
}

~~~

Para cada caso o programa vai executar uma determinada ação.

Por exemplo:

~~~Javascript

switch (tipofruta) {
   case "Laranja":
      console.log("O quilo da laranja está R$0,59.<br>");
      break;
   case "Maçã":
      console.log("O quilo da maçã está R$0,32.<br>");
      break;
   case "Banana":
      console.log("O quilo da banana está R$0,48.<br>");
      break;
   case "Cereja":
      console.log("O quilo da cereja está R$3,00.<br>");
      break;
   case "Manga":
      console.log("O quilo da manga está R$0,56.<br>");
       break;
   case "Mamão":
      console.log("O quilo do mamão está R$2,23.<br>");
      break;
   default:
      console.log("Desculpe, não temos " + tipofruta + ".<br>");
}
console.log("Gostaria de mais alguma coisa?<br>");

~~~