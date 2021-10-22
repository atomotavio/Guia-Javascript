# Manipulação de erros

Voce pode chamar uma exceção usando a declaração throw e manipulá-la usando a declaração try...catch.

## Tipos de exceções

### Throw

voce pode utilizar o throw com qualquer objeto javascript. Porém nem todos os objetos ativados por throw serão igualmente criados.

Voce utiliza uma declaração throw para lançar uma exceção, como por exemplo um erro personalizado.

Se voce quer que um erro seja mostrado para um determinado valor de variavel por exemplo.

~~~Javascript

throw expressão;

~~~

~~~Javascript

throw "Error2";   // tipo string
throw 42;         // tipo numérico
throw true;       // tipo booleano
throw {toString: function() { return "Eu sou um objeto!"; } };

~~~

~~~Javascript

// Cria um objeto do tipo UserException
function UserException(mensagem) {
  this.mensagem = mensagem;
  this.nome = "UserException";
}

// Realiza a conversão da exceção para uma string adequada quando usada como uma string.
// (ex. pelo console de erro)
UserException.prototype.toString = function() {
  return this.name + ': "' + this.message + '"';
}

// Cria uma instância de um tipo de objeto e lança ela
throw new UserException("Valor muito alto");

~~~

### Try... catch

É um bloco de declaração para tratar erros. No caso o durante a execução do código, ele tentará executar o bloco try, caso algum erro ocorra ele exibirá uma mensagem de erro ao usuário definida no bloco catch.

Exemplo:

~~~Javascript

function getMonthName(mo) {
  mo = mo - 1; // Ajusta o número do mês para o índice do array (1 = Jan, 12 = Dec)
  var months = ["Jan","Feb","Mar","Apr","May","Jun","Jul",
                "Aug","Sep","Oct","Nov","Dec"];
  if (months[mo]) {
    return months[mo];
  } else {
    throw "InvalidMonthNo"; //lança uma palavra-chave aqui usada.
  }
}

try { // statements to try
  monthName = getMonthName(myMonth); // função poderia lançar uma exceção
}
catch (e) {
  monthName = "unknown";
  logMyErrors(e); // passa a exceção para o manipulador de erro -> sua função local.
}

~~~

### Finally

Um bloco que será executado independentemente do resultado do try... catch. Por exemplo a limpeza de um campo input.

~~~Javascript

function f() {
  try {
    console.log(0);
    throw "bogus";
  } catch(e) {
    console.log(1);
    return true; // essa declaração de retorno é suspensa
                 // até que o bloco finally seja concluído
    console.log(2); // não executa
  } finally {
    console.log(3);
    return false; // substitui o "return" anterior
    console.log(4); // não executa
  }
  // "return false" é executado agora
  console.log(5); // não executa
}
f(); // exibe 0, 1, 3; retorna false

~~~