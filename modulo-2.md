#  :pushpin: Módulo 2 - Programação Orientada a Objetos (POO)

Neste módulo foram abordados os conceitos de:
  
1. [Introdução](#introdução);
1. [Classe, Objeto e Instância](classe,-objeto-e-instância);
1. Instância e Construtores;

## Introdução

Orientação a Objetos surgiu na década de 1960/1970.

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

**Conceito** - Abordagem usada em Java para definir o formato de um objeto
 - Classe **não** é objeto;
 - Classe **não** é orientação à objetos;

Classes são como Receita ou uma “Planta baixa” que descreve atributos
e comportamento que todas as instâncias desta classe devem possuir. (- SLIDE)

Uma classe é definida pelos seus membros:
- Atributos
- Construtores
- Métodos

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

*Em Java, cada classe deve ser definida em um arquivo que tem o mesmo nome da classe.<br>
Ex: O arquivo com a definição da classe Livro deve ser salvo com o nome `Livro.java`* (- SLIDE)

O poder de **abstração** é muito importante ao definir as classes de um sistema!<br>
A classe deve ser capaz de **representar** o objeto real, mas **apenas para as necessidades daquele sistema específico**. (- SLIDE)
