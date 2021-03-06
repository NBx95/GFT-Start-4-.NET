#### Conhecendo o C#. 

Objetivos da Aula: 


1. O que é C# ? 

Linguagem que surgiu junto com o.NET no começo dos anos 2000. C# é uma lingaugem elegante, orienta a objeto e fortemente tipada. A sintaxe do C# é similar a do C, C++ ou Java. Suporta os conceitos de encapsulamento, herença e polimorfismo (OO).
Os programs C# são executados no .NET, que inclui: 
-CLR (Common Language Runtime)
-Conjunto unificado de bibliotecas de classes. 
Atualmente o compilador do C# é o Roslyn, open source, com o código aberto no GitHub.  


2. Como funciona ?

O código-fonte escrito em C# é compilado em uma linguagem intermediária (IL). O código e os recursos de IL são armazenados no disco em um arquivo executável chamado assembly, geralmente com uma extensão .exe ou .dll. 
Quando o programa C# é executado, o assembly é carregado no CLR. Em seguida o CLR executará a compilação 'Just in Time' (JIT) para converter o código IL em instruções de máquinas nativas. 
O CLR também fornece outros serviços: 
- Garbage Collector.
- Exception Handler.
- Resources Manager. 
Além dos serviços de tempo de execução, o .NET também inclui uma extensa biblioteca com milhares de classes que fornecem uma ampla variedade de funcionalidade úteis, desde entrada e saída de arquivos, manipulação de cadeias de caracteres, análise XML, etc.


3. Estrutura de programa. 

Os principais conceitos organizacionais em C# são: 
- programas.
- namespaces.
- tipos.
- membros.
- assemblies. 

Programas C# consistem em um ou mais arquivos. Os programas declaram tipos, que contêm membros e podem ser organizados em namespaces. 
Classes e interfaces são exemplos de tipos. Campos, métodos, propriedades e eventos são exemplos de membros. 
Quando os programas C# são compilados, eles são fisicamente empacotados em assemblies. 
Os assemblies geralmente têm a extensão de arquivo .exe ou .dll, dependendo se são aplicações ou bibliotecas. 

Exemplos Práticos: Salvos pelo VSCode. 
Faça um debug: leia linha a linha e entenda oq acontece. 
Quando você sobe sua aplicação no VSCode para configurações prédefinidas com o modo debug. 
Extouro de sessão/buffer: Quebrando a regra de exeção. 


Tipos de valor & Tipos e variáveis: 

#### Variáveis do tipo de valor:

Variáveis de tipos de valor contêm diretamente seus dados. (separa um determinado valor de dados na memória, a própria variável contêm seus dados)
As variáveis têm sua própria cópia dos dados e não é possível que as operações afetam outra variável (exceto no caso das variáveis de parâmetro ref e out)
- Numérico: sbyte, short, int, long, byte, ushort, uint, ulong
- Caracteres Unicode: char
- Pontos Flutuantes: float, double, decimal
- Booleano: bool, enum, strucu e tipos nullable (exemplo int?)

#### Variáveis de referência:

Variáveis de tipos de referência armazenam referências a seus dados. (elas não têm os dados diretamente juntos com elas ali na memôria, elas guardam a ultima referência pra esses dados e esses dados são armazenados em um outro espaço da memôria)
É possível que duas variáveis façam referência ao mesmo objeto e, portanto, que operações em ima variável afetem o objeto referenciado pela outra variável.
- Tipos Classe: class, object, string
- Tipos Arrays:int[], int[,], etc...
- interface, delegate.

#### Instruções. 
Ações de um programa são expressas usando instruções 
{ 
Um bloco permite que várias instruções sejam escritas em contextos
}

(que nós podemos agrupar essas ações, essas instruções dentro de um contexto "bloco" que geralmente é delimitado por chaves { }, 
no C# assim como na linguâgem JAVA por exemplo, você pode utilizar chaves { }, pra especificar um bloco de código e ter as instruções ali dentro) 

#### No C# quando falado em instruções, falamos de: 

-Declaração de variáveis e constantes locais
- if, switch:

se algo for A eu faço A, se não for A, eu faço B...
- while, do, for, foreach: Instruções de repetição (loops)
- break, continue, return: Auxiliam a trabalhar dentro das instruções anteriores. 
- throw, try... catch..finally: Instruções para tratativas de exceptions.
- using: Dentro de uma classe importar pacotes a namespaces dentro de nosso projeto.


#### Arrays.: Aula pratica, pelo VSCode... C# o nome da pasta com os códigos fornecidos pelo github do prof: Gabriel Faraday

program.cs = como cada instrução pode ser usada baseados nas informações da aula anterior. 

(variavél "const" n se é possivél alterar os valores, só para quando tiver uma lógica para isso.)
(int a; > a = 1; :: pode-se alterar o valor de acordo é inserido a ele no código.)

args.Length : comprimento. 
(caso seja 0, imprime na tela, nenhum argumento...)

Um array é uma estrutura de dados que contém um número X de elemtnso, todos do mesmo tipo, que são acessados através de índices computados. 
Arrays são tipos de referência e a declaração de uma variável array simplesmente reserva espaço para uma referência de uma instância de array. 
Ao criar um array é especificado o tamanho da nova instância, que é fixo durante todo tempo de vida dessa instância. 
Os índices dos elementso de um array variam de 0 a comprimento do array - 1. 

```
#####Array unidimensional: 

int [] a = new int [10];
  for (int i = 0; i < a.Length; i++)
  {
    a[i] = i * i;
  }
  for (int i = 0; i < a.Length; i++)
  {
    Console.WriteLine($"a[{i}] = {a[i]}");
  }

#####Array multidimensional (matrizes);

int [,] a2 = new int [10, 5]; 
int [,,] a3 = new int [10, 5, 2];

#####Inicializador de Array:

int [] a = new int [] {1, 2, 3}; 
int [] a = {1, 2, 3};

int [] t = new int [3]; 
t[0] = 1; 
t[1] = 2; 
t[2] = 3; 
int[] a = t; 
```

Classes e objetos essenciais em C#: 

O que são Classes e Objetos em C#: 
- Classes e Objetos: Classes são os tipos mais fundamentais de C#, uma classe é uma estrutura de dados que combina estado (campos) e ações (métodos). 
- Objetos são instâncias de uma classe, as classes suportam herança e polimorfismo, mecanismos pelos quais as classes derivadas podem estender e especializar as classes base. 


public class Ponto
```
{
  public int x, y;
  public Ponto (intx, int y)
  {
    this.x = x;
    this.y = y;
  }
}
```
Instâncias de classes (objetos) são criadas usando o operador new, que aloca memória para uma nova instância, chama um construtor para inicializar a instância e retorna uma referência à instância. 

Ponto p1 = new Ponto (0, 0);
Ponto p2 = new Ponto (10, 20);
	
A memória ocupada por um objeto é recuperada automaticamente quando o objeto não está mais acessível. 
Não é necessário nem possível desalocar explicitamente objetos em C#. 

Os membros de uma classe podem ser estáticos ou membros da instância. Membros estáticos pertencem a classe e membros de instância pertencem ao objeto. 
Constantes, variáveis, métodos, propriedades, construtores, etc...

Acessibilidade: Cada membro de uma classe tem uma acessibilidade associada, que controla as regiões do texto do programa que podem acessar o membro. 
Podem ser: 
- public
- protected 
- internal
- private

Herança: Uma declaração de classe pode especificar umma classe base, herdando os membros "public, internal e protected da classe base". 
Omitir uma especificação de classe base é o mesmo que derivar do tipo object. 

Métodos: Um método é uma membro que implementa uma computação ou ação que pode ser executada por um objeto ou classe, (sempre usar verbos para nomear os métodos). 
Os métodos podem ter uma lista de parâmetros, que representam valores ou referências de variáveis passadas para o método, é um tipo de retorno que especifica o tipo do valor calculado e retornado pelo método. 

Como aplicar Classes e Objetos em projetos: 

Só pode assim herdar de uma única class.

VIRTUAL: permite que uma classe filha, sobrescreva a atuação do método. 
OVERRIDE: sobrescreva o método, realizando outra ação. 
