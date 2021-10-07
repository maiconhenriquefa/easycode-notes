# modulo-1
------
## *1. Algoritmos*

Os algoritmos possuem uma sequencia lógica em ordenação e finita. Além disso, não é ambíguo no que diz respeito que é entendido da mesma forma pelas outras pessoas.

<b>exemplo:<b>

<img src="https://slideplayer.com.br/slide/44194/1/images/11/Algoritmos+Abaixo+segue+um+exemplo+simples+de+algoritmo%2C+para+a+troca+de+um+pneu+furado%3A+desligar+o+carro..jpg" alt="Algoritmo-pneu-furado" width="400"/>

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
  
  Exercício:
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
