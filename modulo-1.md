# modulo-1
------
## *1. Algoritmos*

Os algoritmos possuem uma sequencia lógica em ordenação e finita. Além disso, não é ambíguo no que diz respeito que é entendido da mesma forma pelas outras pessoas.

Exemplo (Algoritimo para trocar uma lâmpada):

1. Pegar uma escada;
2. Pegar uma lâmpada nova;
3. Subir degraus "enquanto" não conseguir alcançar a lâmpada;
4. Tirar lâmpada antiga;
5. Colocar lâmpada nova;
6. Descer degraus "enquanto" não conseguir alcançar o chão;

## *2. Variáveis*

"Corresponde a uma posição na memório do computador que armazena um determinado dado que pode ser modificado ao longo do programa".
  
### Formação de identificadores
  - O nome de uma variável deve iniciar com uma letra;
  - Os demais caracteres podem conter números, letras ou "_";
  - Não pode utilizar palavras reservadas da linguagem. Ex: and, from, as, True, False ...;
  - Boa pratica que o nome dos identificadores façam sentido com a informação armazenada;
  
### Declaração
  - Identificador: Nome dado aos "objetos" utilizados no programa (ex: area);
  - Atribuição: Comando que define ou redefine o valor armazenado em uma variável ("=");
  - Expressão: Valor ou conjunto de comandos que resulta em um valor (ex: 2*2);

Ex: area = 2 * 2;
  
  Exercício (Linguagem Java):
~~~java
    public class Main
{
	public static void main(String[] args) {
		int idade = 25;
		string nome = "Maicon Henrique";
		
		string sobrenome = nome;
	}
}
~~~
