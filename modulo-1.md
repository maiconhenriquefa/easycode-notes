#  :pushpin: Módulo 1 - Fundamentos de Introdução a Programação

Neste módulo foram abordados os conceitos de:
  
1. [Algoritmos](#algoritmos)
2. [Variáveis](#variáveis)
3. [Tipos de Dados Fundamentais](#tipos-de-dados-fundamentais)
4. [Operadores, Expressões e Comandos](#operadores,-expressões-e-comandos)
5. [Estruturas Condicionais - Condicional simples](#estruturas-condicionais)
7. [Modularização](#modularização)

## *1. Algoritmos*

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

## *2. Variáveis*

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

## *3. Tipos de dados*

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

## *4. Operadores, Expressões e Comandos*

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
