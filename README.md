# JS I
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

## Função Anônima exemplo 2
const eNumeroPar = function(num) {
  return num % 2 === 0;
};

console.log(eNumeroPar(4)); // Retorna true
console.log(eNumeroPar(5)); // Retorna false


# Arrow Function

// Arrow function

const proximoNum = (n) => {

    return (n + 1)

}
Console.log(proximoNum(6))
outro exemplo so que simplificado:
const vezesCinco = num => num * 5

console.log(vezesCinco(5))

# Seletores DOM
A ligação do DOM com nossos arquivos HTML é de dupla mão: quando um elemento HTML é criado, uma representação dele no DOM é criado, e se alteramos alguma representação no DOM seu respectivo elemento HTML sofrerá as mesmas alterações no navegador.

# Acessando a DOM por ID e Classe
Este objeto tem uma série de propriedades que nos retornam informações sobre nossa página, como por exemplo a URL, ou os cookies.

Usaremos quatro métodos (funções guardadas em um objeto) para acessar os elementos da DOM. Os dois primeiros são:

getElementById() ----> Retorna o elemento que tem o ID com o valor especificado.
getElementsByClassName() -----> Retorna um HTMLCollection com todos os elementos que contem a class especificada.

## Exemplo
const titulo = document.getElementById("titulo");

console.log(titulo) // mostrará o conteudo do titulo lá no HTML

# Acessando a DOM com seletores CSS
Para fazer isso , usaremos os seguintes dois métodos:

querySelector() ---> Retorna o primeiro elemento no documento que segue  a especificação de um seletor CSS.
querySelectorAll() ----> Retorna uma NodeList com todos os elementos no documento que seguem a especificação de um seletor CSS.

## Exemplo
const segundoTitulo = document.querySelector("div h2");
console.log(segundoTitulo); // Mostrará o conteudo da div h2 no HTML

Observações:
Quando usamos os métodos .getElementsByClassName() e .getElementById() passamos apenas
o nome da classe e do id respectivamente. Já quando usamos os métodos .querySelector() e .querySelectorAll() precisamos colocar um ponto '.'antes das classes, e um '#' antes dos IDs.

# innerText e innerHTML

innerText -- Retorna o texto sem formatação e sem elementos HTML.
innerHTML -- Retorna o texto com formatação e com elementos HTML.

## Manipulando o DOM com innerText
Podemos alterar, por exemplo, o texto do nosso elemento h2 acessando a propriedade innerText do elementoH2 e atribuindo a ele um novo valor com o operador de atribuição =, seguido do texto como uma string (escrito entre aspas simples ou duplas).

## Exemplo:
let elementoH2 = document.querySelector(`h2`);

elementoH2.innerText = `Novo Titulo com JS`;
//No exemplo acima o texto antigo em h2 seria substituido por 'Novo Titulo com JS'

As propriedades innerText e innerHTML são simples e nos permitem manipular os elementos do DOM de forma muito ampla. Como orientação geral, é recomendado usar a propriedade innerText quando queremos mudar apenas o texto de um elemento HTML que não possui elementos filhos, pois, caso existam, eles serão substituídos pelo novo texto.
Já a propriedade innerHTML é melhor ser usada quando queremos alterar o conteúdo HTML de qualquer elemento do DOM, podendo incluir os elementos filhos, nomes de classe e qualquer outro atributo que os elementos HTML possam receber.

# Criando elementos no DOM

Para essa ação  estaremos usando os métodos createElement e appendChild.

Exemplo de criação de um elemento li + manipulação criando uma id para o mesmo.
let elementoJavaScript = document.createElement(`li`); //criação da li e da variavel

elementoJavaScript.innerText = `JavaScript` // Manipulação da variavel adicionando o texto entre ``
elementoJavaScript.id = `ling-js` // Adição de um id ao nosso elemento... visto que no html, cada um das li tinha um id

console.log(elementoJavaScript); //Mostraria no console as mudanças realizadas...

---------------------------------------------
let elementoJavaScript = document.createElement(`li`); //criação da li e da variavel

elementoJavaScript.innerText = `JavaScript` // Manipulação da variavel adicionando o texto entre ``
elementoJavaScript.id = `ling-js` // Adição de um id ao nosso elemento... visto que no html, cada um das li tinha um id

//Adicionando o elemento ao site.
// precisamos capturar o seu elemento pai via DOM e salvá-lo em uma variável

let listaLinguagens = document.querySelector(`.lista-linguagens`);
//Com o elemento da lista não ordenada salvo na variável listaLinguagens, podemos chamar essa variável e usar o método appendChild() para adicionar elementos nele.

listaLinguagens.appendChild(elementoJavaScript); // na minha pagina web agora teria o acrescimo de uma li com o texto Javascript... conforme criação acima.

---------------------------------------------------
# Adição de elementos complexos

Para não precisar criar três elementos diferentes (div, h2 e p) e manipular cada um deles adicionando textos e classes, criaremos apenas um elemento e usaremos a propriedade innerHTML, seguindo as mesmas três etapas do exemplo anterior.

const postagemJavaScript = document.createElement(`div`); //onde é criado uma div...

## Usamos a propriedade innerHTML para inserir todo o conteúdo HTML das postagens em um template string:
postagemJavaScript.innerHTML =

`<h2 class="post-titulo">JavaScript</h2>

<p class="post-texto">

  JavaScript é uma linguagem de programação

</p>`
//Nessa etapa, capturamos o elemento pai da nossa postagem e salvamos ele em uma variável:
const postagens = document.querySelector(`.postagens`); //essa classe postagens seria o id da minha section no html

//Nele, adicionamos o elemento postagemJavaScript através do método appendChild().
postagens.appendChild(postagemJavaScript);

Os métodos **createElement()** e **appendChild()** são muito úteis em duas situações: quando queremos popular nosso site com dados vindo de sistemas externos e quando queremos que a interação de nossos usuários altere o conteúdo do site
---------------------------------------------------------------------------------------
# JS II
Segunda parte do conteúdo fornecido pela Proz
## Intro
A linguagem JavaScript nos permite acessar e manipular diretamente a estilização de qualquer elemento capturado no DOM usando a propriedade style. Dessa forma, conseguimos editar nossos elementos com as mesmas propriedades e valores usados na CSS, mas respeitando a sintaxe da linguagem JavaScript.

## Sintase e convenções de escritas

As propriedades do objeto “Style” são escritas com uma única palavra e redigidas da mesma forma que as escreveríamos em um arquivo CSS, por exemplo: color, margin, display etc. Contudo, as propriedades, que têm nomes com mais de uma palavra, seguem padrões de escrita diferentes.
Na linguagem CSS, as escrevemos usando a padronização snake-case, já na linguagem JavaScript, usamos a camelCase. Dessa forma, as propriedades como background-color vira backgroundColor e text-decoration vira textDecoration.

## Manipular classes com a propriedade .classList
A propriedade style é útil quando queremos realizar estilizações menores, ou seja, quando vamos manipular uma propriedade CSS por vez. Porém, se quisermos manipular várias propriedades de uma só vez, é mais prático definir classes com várias regras de estilização e usar a linguagem JavaScript para manipular as classes que cada elemento inclui.

Para manipular listas de classes com JavaScript, primeiro devemos ir no arquivo script.js, capturar o elemento div do DOM e, por fim, salvá-lo em uma variável.

exemplo: let div = document.querySelector("div");

Após isso, use o dot notation para acessar a propriedade classList do elemento que acabamos de salvar. Essa propriedade é um objeto com métodos, que também podemos acessar usando o dot notation.
Agora, vamos usar o método contains(). Ele verifica se um elemento possui ou não uma determinada classe e retorna um valor booleano.

## Verificar se um elemento tem uma classe.

O método contains() recebe como argumento uma string com o nome da classe. Dessa forma, o retorno será true se o elemento conter essa classe e, caso não a possua, será false.

 

Nesse exemplo, passaremos o valor borda-azul, salvaremos o valor retornado pelo método em uma variável chamada incluiClasse e, por fim, usaremos a função console.log() para imprimir o resultado.

**let div = document.querySelector("div")**
 
**let incluiClasse = div.classList.contains("borda-azul")**

**console.log(incluiClasse);**


