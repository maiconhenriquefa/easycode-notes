#  :pushpin: Módulo 2 - Programação Orientada a Objetos (POO)

>Navegação
<ul>
<li><a href="https://github.com/maiconhenriquefa/easycode-notes">Principal</a></li>
<li><a href="https://github.com/maiconhenriquefa/easycode-notes/blob/main/modulo-1.md">Módulo-1</a></li>
</ul>

Neste módulo foram abordados os conceitos de:
  
1. [Introdução](#introdução);
1. [Classe, Objeto e Instância](#classe-objeto-e-instância);
1. [Instância e Construtores](#instância-e-construtores);
2. [Métodos](#métodos);
3. [Encapsulamento](#encapsulamento);
4. [Herança](#herança);
5. [Polimorfismo](#polimorfismo);
6. [Pacotes](#pacotes);
7. [Classes e métodos abstratos](#classes-e-métodos-abstratos);
8. [Interfaces](#interfaces);

## Introdução

Orientação a Objetos surgiu na década de 1960/1970. Onde definem o objeto como entidade.

- Porque estudar Orientação a Objetos?
	- Modularização do código
	- Evita código macarrônicoClasse, Objeto e Instância

- Código modularizado geralmente é:
	- Reusável
	- Fácil de manter
	- Fácil de entender

*\*Benefícios como <ins>Reuso</ins> e <ins>Manutenção</ins> são grandes motivadores para utilizar POO*

## Classe, Objeto e Instância

### Classe

Abordagem usada em Java para definir o formato(modelo) de um objeto, ou seja estamos dizendo como o objeto irão funcionar.
- Classe **não** é objeto;
- Classe **não** é orientação à objetos;

---
**NOTAS**

Classes são como Receita ou uma “Planta baixa” que descreve atributos
e comportamento que todas as instâncias desta classe devem possuir. >(Fonte: Slide)

As classes servem tanto para encapsular informações como também para organizar e modularizar as aplicações.

---


Uma classe é definida pelos seus membros:
- **Atributos (ou campo/propriedade)**
~~~JAVA
[modificador] [tipo] nome = [valor]
~~~
- **Construtores**
~~~JAVA
[modificador] nomeDaClasse{
    ContrutorComNomeDaClasse(parametos){
    	//corpo();
    };
}
~~~
- **Métodos**
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

>*Em Java, cada classe deve ser definida em um arquivo que tem o mesmo nome da classe.<br>
>Ex: O arquivo com a definição da classe Livro deve ser salvo com o nome `Livro.java`* (Fonte: Slide)

---
**NOTAS**

O poder de **abstração** é muito importante ao definir as classes de um sistema!<br>
A classe deve ser capaz de **representar** o objeto real, mas **apenas para as necessidades daquele sistema específico**. >(Fonte: Slide)

---

### Objeto

É tudo que é manipulado ou então, que pode ser. >(fonte: Aurélio)

- Toda classe é um Object.
- Objetos sempre serão compostos de **Atributos**(propriedades) e **Comportamentos**(funções)*
- O objeto pode ser fomado por **n** objetos.*
- **Função**, ou então método, compreende tudo que o objeto faz.

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

`this` - é uma palavra reservada utilizada para acessar a própria instância. >(Fonte: Slide)

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

Conceitua-se encapsulamento como sendo o processo utilizado para proteger os campos e operações de uma classe (atributos e métodos), permitindo que apenas os membros públicos. >(Fonte: CPC Cetec)

- Abstrair como o valor está sendo armazenado para os usuários da classe.
- Apenas código da própria classe deve ser capaz de alterar valores que definem o estado do objeto.
>(Fonte: Slide)

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

>(Fonte: Devmedia)

- `super` : Esse comando indica que você está utilizando um método de uma super classe.

## Pacotes

Deixar todas as classes misturadas na raiz do projeto seria um pesadelo em termos de manutenção. Por isso temos os pacotes.

A API de Java oferece um grande número de classes pré-definidas (como a classe String, por exemplo!), organizadas em pacotes.

A classe Scanner, por exemplo, está no pacote java.util
•Classes de coleções, como ArrayList, HashMap e Stack também estão no pacote java.util

O pacote java.math disponibiliza classes relacionadas a manipulação matemática

- O pacote é chamado pelo seu caminho.
Exemplo:
~~~JAVA
package pasta.subpasta
//Caso fosse para procurar nessa pasta. Contudo abaixo ja estamos em um pacote padrão do Java.

import java.util.ArrayList;

public class Main {
    Private ArrayList<String> autrores;
}
~~~

Geralmente você irá agrupar classes similares em um mesmo pacote.
•Ajuda a organizar o código
•Tem vantagens para manutenção e extensão
(Fonte: Slide)

## Classes e métodos abstratos
A abstração de dados é o processo de ocultar certos detalhes e mostrar apenas as informações essenciais ao usuário.


A `abstract` palavra-chave é um modificador sem acesso, usado para classes e métodos:

- **Classe abstrata**: é uma classe restrita que não pode ser usada para criar objetos (para acessá-la deve ser herdada de outra classe).
- **Método abstrato**: só pode ser usado em uma classe abstrata, e não possui corpo. O corpo é fornecido pela subclasse. Onde é obrigatória sua declaração. (herdado de).

>(Fonte: w3schools)

Exemplo:
~~~JAVA
abstract class Conta {

	private double saldo;

	public void setSaldo(double saldo) {
		this.saldo = saldo;
	}

	public double getSaldo() {
		return saldo;
	}

	public abstract void imprimeExtrato();

}
~~~

## Interfaces

Outra forma de obter abstração em Java é com interfaces.

**Por que Outra forma de obter abstração em Java é com interfaces.e quando usar interfaces?**
1) Para alcançar a segurança - oculte certos detalhes e mostre apenas os detalhes importantes de um objeto (interface).

2) Java não suporta "herança múltipla" (uma classe só pode herdar de uma superclasse). No entanto, isso pode ser alcançado com interfaces, porque a classe pode implementar várias interfaces. Nota: Para implementar várias interfaces, separe-as com uma vírgula (veja o exemplo abaixo).

Para acessar os métodos da interface, a interface deve ser "implementada" (meio como herdada) por outra classe com a `implements` palavra - chave.

Exemplo:
~~~JAVA
// Interface
interface Animal {
  public void animalSound(); // interface method (does not have a body)
  public void sleep(); // interface method (does not have a body)
}

// Pig "implements" the Animal interface
class Pig implements Animal {
  public void animalSound() {
    // The body of animalSound() is provided here
    System.out.println("The pig says: wee wee");
  }
  public void sleep() {
    // The body of sleep() is provided here
    System.out.println("Zzz");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig();  // Create a Pig object
    myPig.animalSound();
    myPig.sleep();
  }
}
~~~

- Assim como as classes abstratas , as interfaces não podem ser usadas para criar objetos (no exemplo acima, não é possível criar um objeto "Animal" em MyMainClass)
- Os métodos de interface não têm corpo - o corpo é fornecido pela classe "implemento"
- Na implementação de uma interface, você deve substituir todos os seus métodos
- Os métodos de interface são por padrão abstracte public
- Os atributos da interface são, por padrão public, staticefinal
- Uma interface não pode conter um construtor (pois não pode ser usada para criar objetos).

>(Fonte: w3schools)

## Exception

Exceções acontecem em Java avisando que ocorreu um problema potencialmente recuperável
- Estende da classe `java.lang.Exception`
- Estende-se de outra classe `java.lang.Throwable`

### Try/Catch/Finally

Para sabermos se uma exceção ocorre podemos utilizar o `if`, mas também podemos utlizar `try`/`cat`
- `try` (tentar): {O que queremos que funcione}
- `catch` (pegar): (passamos o tipo da exceção) {Enão o código é executado se houver uma exceção}
- `finally` (finalmente): {Trecho de código que será executado ao "final" independente de sucesso ou erro no código}

*\*O tipo Exception e serve para todos os tipos de excessões*
*\*Pode-se ter mais de um catch para cada try, contudo em exceções é nescessário observar a hierarquia das classes para que o erro não fique somente no primeiro catch*

### ERRORS

Erros que não possuẽm exceções, que seriam erros irrecuperáveis.

### Throw (lançar)

Para que possamos lançar excessões para comunicar um problema podemos utilizar o `throw`.
ex:
~~~JAVA
if (livro == null) {
	throw new Exception("mensagem");
}
~~~
------
Exceções
- **Checked**: azul na imagem abaixo
- **Unchecked**: amarelos na imagem abaixo

![image](https://user-images.githubusercontent.com/53382761/138131876-2ba75ecc-fa5e-4eaf-9f6e-14a5e1632582.png)

