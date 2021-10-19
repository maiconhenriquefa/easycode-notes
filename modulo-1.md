#  :pushpin: Módulo 1 - Fundamentos de Introdução a Programação

Neste módulo foram abordados os conceitos de:
  
1. [Algoritmos](#algoritmos)
2. [Variáveis](#variáveis)
3. [Tipos de Dados](#tipos-de-dados)
4. [Operadores, Expressões e Comandos](#operadores-expressões-e-comandos)]
5. [Estruturas de Repetição](#estruturas-de-repetição)
6. [Estruturas Condicionais](#estruturas-condicionais)

## Algoritmos

Os algoritmos possuem uma sequencia lógica em ordenação e finita. Além disso, não é ambíguo no que diz respeito que é entendido da mesma forma pelas outras pessoas.

Exemplo (Algoritimo para trocar uma lâmpada):

1. Pegar uma escada;
2. Pegar uma lâmpada nova;
3. Subir degraus "enquanto" não conseguir alcançar a lâmpada;
4. Tirar lâmpada antiga;
5. Colocar lâmpada nova;
6. Descer degraus "enquanto" não conseguir alcançar o chão;

Primeiro código rodando:

~~~java
public class Main
{
    public static void main(String[] args){

        System.out.println("HELLO WORLD!");
    }
}

// HELLO WORLD!
~~~

`System.out.print` - Print na tela<br>
`ln` - Pula para próxima linha<br>

## Variáveis

"Corresponde a uma posição na memório do computador que armazena um determinado dado na memória RAM (traduzido - "Memória de Acesso Aleatório"), onde pode ser modificado ao longo do programa".
  
### Formação de identificadores
  - O nome de uma variável deve iniciar com uma letra;
  - Os demais caracteres podem conter números, letras ou "_";
  - Não pode utilizar palavras reservadas da linguagem. Ex: and, from, as, True, False ...;
  - Boa pratica que o nome dos identificadores façam sentido com a informação armazenada;
  
### Declaração
  - Identificador: Nome dado aos "objetos" utilizados no programa (ex: area);
  - Atribuição: Comando que define ou redefine o valor armazenado em uma variável (`=`);
  - Expressão: Valor ou conjunto de comandos que resulta em um valor (ex: 2*2);

Ex: `area = 2 * 2`;
  
  Exercício (Linguagem Java):
~~~java
    public class Main
{
	public static void main(String[] args) {
		int idade = 25;
		String nome = "Maicon Henrique";
		
		String sobrenome = nome;
	}
}
~~~

## Tipos de dados

Primitivos:
- **Inteiro - `int`** : Valores inteiros (ex: 10,0,-8);
- **Real - `double`** : Valores negativos e positivos e fracionários (ex: 10, 15.5, -8.1);
- **Caractere - `string`** : Texto ("ENTRE ASPAS DUPLAS");
- **Lógico - `boolean`** : Verdadeiro ou Falso.

*Tipo de dado* - *Em Java é nescessário passar o tipo do dado da variável quando for declarar;*<br>
*Ponto e vírgula* - *Sempre ao finalizar a declaração de uma variável deve-se utilizar ponto e vírgula;*<br>
*Case-sensitive* - *Caracteres em caixa alta e em caixa baixa são tratados de modo diferente;*<br>

__"camelCase - `palavrasCompostasSeparandoPelaLetraMaiúscula`"__

Exercícios:
~~~java
    public class Main
{
	public static void main(String[] args) {
		String nomeDoAluno = "Maicon Henrique";
		String descriçãoProduto = "Produto descrição";
		int codigoExpresso = 777878;
	}
}
~~~

~~~java
puclic static void main(String args[])
{
	int idade;
	double altura;
	boolean preparado;
	String nome;
	
	idade = 25;
	altura = 1.83;
	preparadp = true;
	nome = "Maicon Henrique"
}
~~~

**Constantes** (Dados que *não devem ser alterados* durante a execução do programa). Utiliza o `final` na declaração. Boa prática utilizar *CAIXA ALTA*.
~~~java
    public class Main
{
	public static void main(String[] args) {
		final double PI = 3.1416;
		final String NOME_PAGINA = "home";
}
~~~

## Operadores, Expressões e Comandos

### Operadores aritmético:

- Soma - `-`
- Subtração - `+`
- Multiplicação - `*`
- Divisão - `/`

**Assim como na matemática, os operadoderes de multiplicação e divisão tem preferência na expressão, e os parenteses demonstram ainda mais preferência.*

Exercício:
~~~java
public class Main
{
    public static void main(String[] args){
    	final double PESO_NOTA1E2 = 1;
	final double PESO_NOTA3E4 = 1;
    
        double alunoNota1 = 7.5;
        double alunoNota2 = 6.5;
        double alunoNota3 = 10;
        double alunoNota4 = 10;
        int notas = 4;
        
        final double MEDIA_FINAL = (((alunoNota1 + alunoNota2) * PESO_NOTA1E2) + ((alunoNota3 + alunoNota4) * PESO_NOTA3E4)) / notas;
        
        System.out.printf("O resultado da média é: %.2f", MEDIA_FINAL);
    }
}

// O resultado da média é: 8.50
~~~

### Operadores de Igualdade:
(*Retorna valor booleano*)

`==` - Utilizado quando desejamos verificar se uma variável é *igual* a outra;<br>
`!=` - Utilizado quando desejamos verificar se uma variável é *diferente* de outra;<br>

### Operadores de Incremento e Decremento:

`++` - Incremento<br>
`--` - Decremento<br>

### Operadores Relacional
(*Obtem a relação dos membros da esquerda com os da direita)

| Operador | Descrição | Exemplo |
| :--------: | :--------:  | :------: |
| > 	 | Maior que       | 2 < 3 |
| < 	 | Menor que       | 2 > 4 |
| >= 	 | Maior igual que | 2 >= 2 |
| <=	 | Menor igual que | 4 <= 4 |
| !=     | Diferente de    | True != False |
| ==     | Igual a         | True == 1 |

Exercício:
~~~Java
import java.util.*;

public class Main
{
	public static void main(String[] args) {
	    final int VALOR1 = 40;
	    
	    Scanner scan = new Scanner(System.in);
	    
	    System.out.print("Informe um numero inteiro: ");
	    int valorUsuario = scan.nextInt();
	    
	    System.out.println("O resultado da compração é: " + (valorUsuario >= VALOR1));
	}
}


// Informe um numero inteiro: 40
// O resultado da compração é: true
~~~

### Operadores Lógicos

**Conectivo de conjunção:** E (and) - `&&` <br>
As duas condições precisam ser VERDADEIRAS

**Conectivo de disjunção:** OU (or) - `||` <br>
Apenas uma condição precisa ser VERDADEIRA

**Conectivo de negação:** NÃO (not) - `!` <br>
Negará a condição VERDADEIRA ou FALSA

**TABELA VERDADE `&&`**
| BOOLEAN | BOOLEAN | RESULT
| :--------: | :--------:  | :------: |
| FALSE | FALSE | **FALSE**|
| FALSE | TRUE  | **FALSE**|
| TRUE  | FALSE | **FALSE**|
| TRUE	| TRUE  | **TRUE** |

**TABELA VERDADE `||`**
| BOOLEAN | BOOLEAN | RESULT
| :--------: | :--------:  | :------: |
| FALSE | FALSE | **FALSE**|
| FALSE | TRUE  | **TRUE**|
| TRUE  | FALSE | **TRUE**|
| TRUE	| TRUE  | **TRUE** |

## Estruturas Condicionais

### Condicional simples

A estrutura condicional if/else permite ao programa avaliar uma expressão como
sendo verdadeira ou falsa e, de acordo com o resultado dessa verificação, executar uma outra rotina.

`if` - se <br>
`else` - se não <br>

Exemplo em JAVA:

~~~JAVA
if (expressão booleana) {
   //bloco de código 1
} else {
   //bloco de código 2
   }
~~~

### Condicional composta

Para mais de uma condição à estrutura de decisão podemos adicionar ao `else if`.

Exemplo em JAVA:

~~~JAVA
if (expressão booleana) {
   //bloco de código 1
} else if {
   //bloco de código 2
   }
} else {
   //bloco de código 3
   }
~~~

Conforme podemos ver no exercício a seguir:

~~~JAVA
import java.util.*;

public class Main
{
	public static void main(String[] args) {
	    Scanner scan = new Scanner(System.in);
	    
	    int golsEquipeA;
	    int golsEquipeB;
	    
	    System.out.print("Informe quantos gols a Equipe A fez: ");
	    golsEquipeA = scan.nextInt();
	    
	    System.out.print("Informe quantos gols a Equipe A fez: ");
	    golsEquipeB = scan.nextInt();
	    
	    if (golsEquipeA > golsEquipeB) {
	        System.out.println("A Equipe A venceu!");
	        
	    } else if (golsEquipeA == golsEquipeB){
	        System.out.println("A Equipe A empatou com a Equipe B!");
	        
	    } else {
	        System.out.println("A Equipe B venceu!");
	    }
	}
}
~~~

Desafio aplicando condicional composta e operadores lógicos:

~~~JAVA
import java.util.*;

public class Main
{
	public static void main(String[] args) {
	    final int CONDICAO1 = 280;
	    final int CONDICAO2 = 700;
	    final int CONDICAO3 = 1500;
	    
	    
	    Scanner scan = new Scanner(System.in);
        double salario = 0;
        double percentual = 0;
        double salarioReajuste = 0;
	    double valorReajuste = 0;
	    
	    System.out.println("Informe o salário do colaborador: ");
	    salario = scan.nextDouble();
	    
	    if(salario <= CONDICAO1){
	        percentual = 20;
	        valorReajuste = salario*1.20;
	        salarioReajuste = valorReajuste - salario;
	    }else if(salario > CONDICAO1 && salario < CONDICAO2){
	        percentual = 15;
	        valorReajuste = salario*1.15;
	        salarioReajuste = valorReajuste - salario;
	    }else if(salario > CONDICAO2 && salario < CONDICAO3){
	        percentual = 10;
	        valorReajuste = salario*1.10;
	        salarioReajuste = valorReajuste - salario;
	    }else{
	        percentual = 05;
	        valorReajuste = salario*1.05;
	        salarioReajuste = valorReajuste - salario;
	    }
	    System.out.println("O salario é: " + salario);
	    System.out.println("O percentual é: " + percentual);
	    System.out.println("Valor real reajustado é: " + salarioReajuste);
	    System.out.println("Valor reajuste: " + valorReajuste);
	}
}
~~~

## Estruturas de Repetição

AS estruturas de repetição, também conhecidas como laços(loops) são utilizadas para executar repetidas vezs uma instrução, sobre determinada condição.

Estrutura: inicialização-condição-corpo e iteração.

### While (enquanto)

~~~JAVA
While(Condição){
	- Comandos
	- Comandos que faça a condição ser satisfeita
}
~~~

### Do - While (faça - enquanto)

~~~JAVA
do{
	- Comandos
	- Comandos que faça a condição ser satisfeita
} while(condição)
~~~

*Diferente do while, o do/while faz o comando antes da condição*

Exercício:
~~~JAVA
import java.util.*;

public class Main {
	public static void main(String[] args) {
	    Scanner scan = new Scanner(System.in);
	    int numeroUsuario =0;
	    
	    System.out.print("Informe um número de 0 à 10: ");
	    numeroUsuario = scan.nextInt();
	    
	    while(numeroUsuario<0 || numeroUsuario>10){
	        System.out.print("Informe um número correto de 0 à 10: ");
	        numeroUsuario = scan.nextInt();
	    };
	    
	    System.out.print("Nota informada corretamente: "+numeroUsuario);  
	}
}
~~~

### For (para)
~~~JAVA
for(inicialização, condição, iteração){
	- comandos
}
~~~

*For é uma estrura de repetição mais compacta, onde a inicialização, condição e iteração são declarados no cabeçalho*
## Modularização

**Modularização** - *Conceito computacional que é empregado para dividir o seu programa em partes funcionais, partes essas qeu conversam umas com as outras.*

Vantagens:
1. Código mais organizado e legível;
2. Permite uma manutenção mais fácil e rápida;
3. Possibilida o reaproveitamento de código.

### Bloco

**Bloco de instrução** - *São seções de código que serão executados quando invocados ou então, quando uma condição for verdadeira.*

Exemplo de bloco:
~~~JAVA
exemplo() {
    trecho de código
}
~~~

### Procedimento e Função

**Procedimento** - São estruturas que agrupam um conjunto de comandos, que são executados quando o procedimento é chamado (Não retorna um resultado)

~~~JAVA
public static void exebirResultatdo(int resultado) {
    System.out.println("A soma foi: " + resultado);
}
~~~
`void` (vazio) - Utilizado para o procedimento. 

**Função** - Tipo especial de procedimento onde depois de executada a chamada, o valor calculado é retornado.

~~~JAVA
public static int somar(int a, int b) {
    return a+b;
}
~~~

**Invocação** - Os valores dos argumentos são copiados para a função/procedimento chamado.

 ~~~JAVA
resultadoOperacao = somar(num1, num2);
exibirResultado(resultadoOperacao);
~~~

### Escopo

**Conceito** - O escopo de uma variável éa parte do programa que pode acessar uma variável. Quando se tenta acessar uma variável que não está no escopo, normalmente se têm um erro do compilador.

**Escopo Global** - Uma variável global é declarada fora das funções e pode ser acessada por todas as funções presentes no módulo onde é definida.

**Escopo Local** - Uma variável local existe apenas dentro da função onde foi declarada. As variáveis locais são inicializadas a cada nova chamada à função.
