# Instruções
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
a) A saída será undefined seguido de erro. 

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

Resposta: a) A saída será undefined seguido de erro <br>
Explicação: Em primeiro momento a saída é undefined já que o JavaScrpit segue uma ordem sequêncial de comandos e como a variável x foi declarada com "Var", uma variável global, ela já existe no programa, porém não está definida quando x é exibido no console. Já em segundo momento acontece erro pela mesma lógica de x, em que y tende a ser impresso no console antes de ser declarado, porém por conta dele ter sido declarado com "let" ele ainda não existe no programa e por isso a mensagem de erro é apresentada. 


**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

Resposta: b) Substituir if (a || b === 0) por if (a === 0 && b === 0) <br>
Explicação: Os operadores lógicos separam grupos de condição e, portanto, os grupos da estrutura condicional if são: (a) e (b === 0). Logo, ao se tratar de pelo menos uma condição verdadeira como base para expressar " return "Erro: número inválido";" ao imprimir "a", sem nenhuma condição, a liberação do comando é sempre verdadeira. Ao substituir por dois novos grupos que precisam ser iguais a 0 o problema do parâmetro "a" é resolvido, ja que agora ele passa a receber uma condição.  

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

b) O código imprime 200.

c) O código imprime 50.

d) O código gera um erro.

Resposta: b) O código imprime 200. <br>
Explicação: A estrutura de loop "Switch" roda em sequência todos os seus casos. A questão imprime o valor errado já que não existe o elemento Break, no caso de "Eletrônico", que interrompe o fluxo de casos quando um deles é atendido. Portanto, mesmo o caso "Eletrônico" existindo, o programa continua rodando e reflete o resultado errado. 
______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

d) 24

Resposta: d) 24
Explicação: Uma lista "numeros" é declarada e guarda dentro de um array alguns números, depois disso uma variável é declarada para abrigar uma série de transformações no array inicial. "numeros.map(x => x * 2) é um método que cria um novo array em que os números originais da lista são dobrados por uma função de seta. "filter(x => x > 5)" também é um método, porém ele seleciona quais valores do array gerados anteriormente irão fazer parte do novo array, no caso são os números maiores que 5, através da função de seta. E por fim, "reduce((a, b) => a + b, 0)" pega todos os elementos do array anterior e reduz em um único valor, sendo o parâmetro "a" o montante, o "b" o elemento a ser somado e o "0" como valor inical da soma. 

______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

c) ["banana", "abacaxi", "manga", "laranja"]

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

Resposta: c) ["banana", "abacaxi", "manga", "laranja"]
Explicação: O método splice aceita argumentos como Início: Em qual indice do array a modificação será iniciada, Remover: Quantos ítens da lista serão removidos apartir do início e Adição de Ítens: Adiciona quais elementos serão acrescentados no array apartir da posição de início. 
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

Resposta: a) As duas afirmações são verdadeiras, e a segunda justifica a primeira. <br>
Explicação: A herança é uma característica comum entre as linguagens de programação tendo em vista a otimização do código e do processo de desenvolvimento, já que uma estrutura não precisa ser reescrita para sua implementação em outras partes do código. A segunda afirmação justifica a primeira uma vez que "extends" é o caminho usado para puxar esse bloco de comandos, conhecido como classe pai, podendo ser alterado ou reutilizado na classe filha. 
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

a) I e II são verdadeiras.

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

Resposta: a) I e II são verdadeiras.
Explicação: A classe Funcionario é uma classe filha que estende a classe Pai, Pessoa, e por isso ela pode acessar seus métodos e atributos. Além disso, o super caracteriza que aquele método, mesmo existindo de maneira diferente na classe filha, é puxado da classe Pessoa. E por fim, a afirmação III é falsa por alegar que o JavaScript não aceita herança de classes. 

______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```
______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.
