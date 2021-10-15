#  :pushpin: Módulo 2 - Programação Orientada a Objetos (POO)

Neste módulo foram abordados os conceitos de:
  
1. [Introdução](#introdução);
1. [Classe, Objeto e Instância](classe,-objeto-e-instância);
1. Instância e Construtores;

## Introdução

Orientação a Objetos surgiu na década de 1960/1970. Onde definem o objeto como entidade.

Porque estudar Orientação a Objetos?
- Modularização do código
- Evita código macarrônicoClasse, Objeto e Instância

Código modularizado geralmente é:
- Reusável
- Fácil de manter
- Fácil de entender

*\*Benefícios como <ins>Reuso</ins> e <ins>Manutenção</ins> são grandes motivadores para utilizar POO*

## Classe, Objeto e Instância

### Classe

**Conceito** - Abordagem usada em Java para definir o formato(modelo) de um objeto, ou seja estamos dizendo como o objeto irão funcionar.

 - Classe **não** é objeto;
 - Classe **não** é orientação à objetos;

Classes são como Receita ou uma “Planta baixa” que descreve atributos
e comportamento que todas as instâncias desta classe devem possuir. (Fonte: Slide) As classes servem tanto para encapsular informações como também para organizar e modularizar as aplicações.

Uma classe é definida pelos seus membros:
- Atributos (ou campo/propriedade) - 
~~~JAVA
[modificador] [tipo] nome = [valor]
~~~
- Construtores
~~~JAVA
[modificador] nomeDaClasse{
    ContrutorComNomeDaClasse(parametos){
    	//corpo();
    };
}
~~~
- Métodos
~~~JAVA
[modificador] [tipo] nome() {
    //corpo();
}
~~~

Exemplo:
~~~JAVA
public class Livro {
    String titulo;
    String[] autores;
    int numPaginas;
    boolean emprestado;
    int qtdEmprestimos;
    int ano;
    String observacoes;
    Pessoa emprestadoPara;
    
    void emprestar(Pessoa pessoa) { /*...*/ }
    void devolver() { /*...*/ }
    String gerarReferencia() { /*...*/ }
    void adicionarObservacao(String novaObs) { /*...*/ }
    
}
~~~

`extends` - A classe pode ser *herdeira* de outra classe. (implicitamente a classe é herdeira da classe Object).

~~~JAVA
public class Livro extends Objetct{
	String título;
	String[] autores;
	int anoPublicacao;
	boolean estaEmprestado;
}
~~~

*Em Java, cada classe deve ser definida em um arquivo que tem o mesmo nome da classe.<br>
Ex: O arquivo com a definição da classe Livro deve ser salvo com o nome `Livro.java`* (Fonte: Slide)

O poder de **abstração** é muito importante ao definir as classes de um sistema!<br>
A classe deve ser capaz de **representar** o objeto real, mas **apenas para as necessidades daquele sistema específico**. (Fonte: Slide)

### Objeto

**Objeto** - É tudo que é manipulado ou então, que pode ser. (fonte: Aurélio)

*Toda classe é um Object.

*Objetos sempre serão compostos de **Atributos**(propriedades) e **Comportamentos**(funções)*

*O objeto pode ser fomado por **n** objetos.*

**Função**, ou então método, compreende tudo que o objeto faz.

## Instância e Construtores 

**Instância** - É a concretização de uma classe. Instanciar uma classe é criar um novo objeto do mesmo tipo dessa classe. (fonte: Devmedia)

- Espaço para armazenar valores para todos os atributos definidos na classe para cada instância
- Cada instância é independente de outras instâncias da mesma classe
(Fonte: Slide)

**Construtores** - Definen como uma instância de uma classe deve ser criada.

- Permitem que as instância estejam em um estado válido desde sua criação.
- Chamados através da keyword `new`.
- Deve-se ter o mesmo nome da classe

~~~JAVA
public Livro(String titulo, String autor, int ano){
    this.titulo = titulo;
    this.autores = new Autor[1];
    autor[0] = autor;
    this.ano = ano;
}
    
    //...Livro novo = new Livro("Dom Casmurro","Machado de Assis", 1899);
~~~

**Construtores sempre exitem; se não forem declarados a classe possuirá um construtor vazio*

### This

`this` - é uma palavra reservada utilizada para acessar a própria instância. (Fonte: Slide)

### Overloading

**Overloading** - Sobrecarga de métodos. São diferenciados pelos tipos de parâmetros.

### Recursividade

**Recursividade** - É uma situação onde uma rotina invoca a si mesma. Ou seja, função que retorna a própria função.
O fenômeno da recursividade sempre irá formar uma pilha até que a expressão seja resumida a sua condição mais simples.

## Métodos

Operações que realizam ações e modificam os valores dos atributos de seu respectivo objeto.

- Especificação (ou cabeçãlho) do método `[modificador] [tipo] nome(parametos)`
- Assinatura do método `nome(parametos)`

***Tipo de retorno* - é obrigatório. Se o método não tem retorno, usar `void`*

## Encapsulamento

**conceito** - Conceitua-se encapsulamento como sendo o processo utilizado para proteger os campos e operações de uma classe (atributos e métodos), permitindo que apenas os membros públicos. (Fonte: CPC Cetec)

- Abstrair como o valor está sendo armazenado para os usuários da classe.
- Apenas código da própria classe deve ser capaz de alterar valores que definem o estado do objeto.
(Fonte: Slide)

### Modificadores de acesso

- `public` - Permite acesso de quakquer uma classe, pacote, subclasse, ou seja, todos o lugares.
- `protected` - Permite acesso:
	- classes no mesmo pacote ou que estão fora mas que estendam desta classe;	
- `package-protected/friendly(defaul)` Permite acesso:
	- Usado se não especificado outro;
	- Permite acesso para outras classes no mesmo pacote private;
- `private` - Permite acesso apenas dentro da própria classe.

![modificadores-de-acesso](https://user-images.githubusercontent.com/53382761/137360714-f9e054f2-0398-4f8c-8617-5cdae84021bc.png)

Para alterações e definições de atributos em uma classe utilizamos muitas vezes o conceito de get(pegue) e set(defina).

**Podemos fazer as seguintes perguntas**

- Seu atributo deve ser apenas lido fora de sua classe, nunca alterado?
	- Não implemente um método set
- Seu atributo possui alguma regra que necessite controle (validação, conversão, etc) ao ter o valor alterado?
	- Implemente o controle no método set
- Seu atributo deve ser apenas alterado fora de sua classe, mas nunca lido (situação incomum, mas existente)?
	- Não implemente um método get

## Herança

Permite que façamos uma reoganização melhor do nosso código reutilizando funcionalidades.
- Classe derivada(subclasse) "possui todo o código" da classe base(superclasse).
- Classe derivada pode alterar o comportamento apenas para instâncias criadas a partir dela, sem comprometer a classe base.

**Superclasse**(classe pai ou base) - Classe da qual as outras classe vão herdar.
**Subclasse**(classe derivada ou filha) - Classe que herda de outra classe.

Ex: `public class NomeDaClasseQueÉAquiASubclasse extends NomeDaClasseQueÉAquiASuperclasse`
*Pode-se ler que a subclasse é uma extensão da superclasse (is-a - relacionamento é um/ ex: onibus is-a veículo / ex: hip-hop is-a música)

## Polimorfismo

Polimorfismo(muitas formas) referese à alteração do comportamento de uma superclasse na subclasse.
- Polimorfismo Estático ou Sobrecarga (Overload)
- Polimorfismo Dinâmico ou Sobreposição (Override)

O **Polimorfismo Estático** se dá quando temos a mesma operação implementada várias vezes na mesma classe. A escolha de qual operação será chamada depende da assinatura dos métodos sobrecarregados.

O **Polimorfismo Dinâmico** acontece na herança, quando a subclasse sobrepõe o método original. Agora o método escolhido se dá em tempo de execução e não mais em tempo de compilação. A escolha de qual método será chamado depende do tipo do objeto que recebe a mensagem.

(Fonte: Devmedia)

- `super` : Esse comando indica que você está utilizando um método de uma super classe.