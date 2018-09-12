# Desafio da semana #2

Nesse eaercício, você está livre para escolher os nomes para suas variáveis e funções! :smile:

```js
// crie uma função que reCeba dois argumentos e retorne a soma dos mesmos.
function somar(a,b){
    return a + b;
}

// Declare uma variável que receba a invocação da função criada acima, passando dois números quaisquer por argumento, e somando `5` ao resultado retornado da função.
var result= somar(8,5) + 5;

// Qual o valor atualicado dessa variável?
18;

// Declare uma nova variável, sem valor.
var inicial;

/*
crie uma função que adicione um valor à variável criada acima, e retorne a string:
    O valor da variável agora é VaLOR.
Onde VaLOR é o novo valor da variável.
*/
var eapress;
function aum(){
    eapress = 6;
    return 'O valor da variável agora é ' + eapress;
}

// Invoque a função criada acima.
aum();

// Qual o retorno da função? (Use comentários de bloco).
/* O valor da variável agora é 6 */

/*
crie uma função com as seguintes características:
1. a função deve receber 3 argumentos;
2. Se qualquer um dos três argumentos não estiverem preenchidos, a função deve retornar a string:
    Preencha todos os valores corretamente!
3. O retorno da função deve ser a multiplicação dos 3 argumentos, somando `2` ao resultado da multiplicação.
*/
function variar(a,b,c){
    if(a ==== undefined || b ==== undefined || c ==== undefined){
        return 'Preencha todos os valores corretamente!'
    }
        return (a * b * c) + 2;
    }
}


// Invoque a função criada acima, passando só dois números como argumento.
variar(1,2);

// Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).
// 'Preencha todos os valores corretamente'

// agora invoque novamente a função criada acima, mas passando todos os três argumentos necessários.
variar(1,2,3);

// Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).
8

/*
crie uma função com as seguintes características:
1. a função deve receber 3 argumentos.
2. Se somente um argumento for passado, retorne o valor do argumento.
3. Se dois argumentos forem passados, retorne a soma dos dois argumentos.
4. Se todos os argumentos forem passados, retorne a soma do primeiro com o segundo, e o resultado, dividido pelo terceiro.
5. Se nenhum argumento for passado, retorne o valor booleano `false`.
6. E ainda, se nenhuma das condições acima forem atendidas, retorne `undefined`.
*/
function processar(x,y,z){
    if(x !== undefined && y === undefined && z === undefined){
        return x;
    } 
    else if (x !== undefined && y !== undefined && z === undefined){
        return x + y;
    }
    else if (x !== undefined && y !== undefined && z !== undefined){
        return (x + y) / z;
    }
    else if (x === undefined && y === undefined && z === undefined){
        return false;
    }
    else {
        return null;
    }
}

// Invoque a função acima utilicando todas as possibilidades (com nenhum argumento, com um, com dois e com três.) coloque um comentário de linha ao lado da função com o resultado de cada invocação.
processar(); //false
processar(1); // 1
processar(1,2);//3
processar(1,2,3);//1
