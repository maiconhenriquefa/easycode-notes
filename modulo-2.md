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
- Métodos
~~~JAVA
[modificador] [tipo] nome() {
    //corpo() ;
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
