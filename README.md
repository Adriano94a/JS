# JS
Conteudo sobre Java Script

# Operadores em JS
soma + , subtração - , multiplicação * , divisão / ,
Modulo % , Maior que > , Menor que < .
# Operadores lógicos
Conjunção (e) = &&
Disjunção (ou) = ||
Negação (not ou) = !

# Condicionais exemplo:
let nota = 9;
if(nota >= 8){

    console.log("Ótimo trabalho!");
}


Sempre que trabalhamos com variáveis que guardam valores booleanos em JS podemos verificar sua “veracidade” apenas chamando o nome da variável. Já se quisermos verificar se o valor do booleano é falso, podemos usar o operador de negação (!) antes do nome da variável:

# Lops em JS
For (exemplo)
for(let i = 0; i < 10; i++){
    console.log(i);
}

# Percorrer um array com 
let letras = ['a','b','c'];
console.log (letras.length);
Imprimira '3' pois o array 'letras' tem três elementos.

Podemos usar a propriedade length para percorrer arrays em JS sem nos preocupar pela quantidade de elementos. Para fazer isso, devemos inclui-lo como condição de parada do nosso for loop da seguinte forma:
let letras = ['a', 'b', 'c'];
for(let i = 0; i < letras.length; i++){
    console.log(letras[i]);
}
// Imprimirá 'a', 'b', e 'c'
-------------------------------------------------------------------------------------------------
# Funçoes
# Função Regular
Segue um exemplo de uma função regular, sem parâmetros, que imprime uma mensagem de boas-vindas quando executada:


function cumprimentar(){
    console.log("Boas-vindas!")
}
cumprimentar();
// Imprimirá "Boas-vindas!"
Obs. Lembra que para executar o bloco de código de qualquer função é necessário declarar ela, e depois chamá-la, escrevendo apenas o nome da função seguida de parênteses (com argumentos, caso precisar deles)
Outro exemplo...
function multiplicar(num1, num2){
    return (num1 * num2);
}
multiplicar(3, 7);
// Imprimirá 21, que é o resultado de (3 * 7)

# Função Anônima
Estas funções não possuem um nome quando declaradas, e são geralmente atribuídas a uma variável que guarda a função como seu valor.
// Função anônima

const adicionar = function(a, b){

      return (a + b);
}
Para chamar uma função anônima, basta chamar o nome da variável que a guarda, seguida de um par de parênteses (com argumentos, caso precisar deles)
const somar = function(a, b){
    return (a + b);
}
Somar(5,9)
// Imprimirá 14, que é o resultado de (5 + 9)

# Arrow Function

// Arrow function

const proximoNum = (n) => {

    return (n + 1)

}
Console.log(proximoNum(6))
outro exemplo so que simplificado:
const vezesCinco = num => num * 5

console.log(vezesCinco(5))


