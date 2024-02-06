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

