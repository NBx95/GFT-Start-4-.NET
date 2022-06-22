### Tipos por Referência & Tipos por Valor. 

#### Objetivo do Curso: 
Entender a diferença entre utilizar variáveis por referência e valor, value type, será fundamental para entender como o compilador executa o código que você escrever. Ou seja, sem entender esse conceito fundamental um desenvolvedor terá muitos problemas para descobrir bugs. 

- Conceitos / Prática
- Palavra chave: ref
- Palavra chave: ref Struct
- Comparação por Valor e por Referência
- Garbage Collector

### Reference Types: Value Types!

Tudo que herda diretamente de System.Object, é tratado como "reference type". 
Tudo que herda diretamente de System.ValueType serão "value types".
       
#### Reference Types.
- System.String
- System.Array
- Base de Classes, Bibliotecas e Interfaces. 
    
#### ValueTypes.
- System.Enum
- System.Int123
- System.Boolean
- Structs, incluindo numeric types.

#### Definindo - Value Types:
- Contém uma INST NCIA do tipo criado. 
- A Instância sempre é copiada ao atribuir o valor para outra variável. 
- Alocação na Stack (melhor performance).
- O valor inicial é sempre o valor default de cada tipo. 

#### Definindo - Reference Types.
- Contém uma REFERÊNCIA para uma instância do tipo criado. 
- A REFERÊNCIA NUNCA MUDA AO ATRIBUIR O VALOR PARA OUTRA VARIÁVEL.
- Na Stack fica um ponteiro e a alocação na HEAP.
- Seu valor inicial é sempre "Null". 
- Requer gerenciamento da Memória através do GC (Garbage Collector). 
- Tipos Primitivos (values types)

*Valores numéricos
 - int
 - decimal 
 - double, etc
*Boolean (true/false)
*Char 
*Tuples 

#### Reference Types.
*Classe 
*Interface 
*Delegate 
*Record 
*Object
*String* [Por não haver limite de tamanho, precisam ser alocadas na heap, para evitar superlotação na stack] 

[AULA PRÁTICA ANOTAÇÕES]
*Foi adicionado a extensão C# e dotnet wrapper ao vsCode de acordo com a indicação do professor, mudamos para o console integrado para melhor visualização do debug com "integratedTerminal". Também criamos um novo código no vsCode, referente a aula. 
Foi feito o uso do "using static System.Console" para encurtar o texto quando for usar (Console.Writeline).* 
   
#### C# II: Value Types 
- Criar uma Console application que receba um valor inteiro na Main; 
- Criar um método void que receba esse inteiro e altere o seu valor para qualquer outro; 
- De volta ao Main exiba no terminal o valor alterado;

``` 
using static System.Console;
using System;
  
  public class Program
  {
    static int Adicionar20(int x)
    {
      return x + 20;
    }
  public static void Main()
  {
      int a = 2;
      a = Adicionar20(a);
      WriteLine($"O valor da variável a é {a}");
  }
}
*Resultando no valor de 22, pois é atribuído o valor da soma a variável 'a'.*
```

#### C# II: Reference Types
Criar uma Console application e uma classe Pessoa com os seguintes atributos: "Nome", "Idade" "Documento";
No Main crie uma instância de Pessoa atribuindo a essas propriedade, seu nome e sua idade;
Crie um método void para alterar o Nome do objeto Pessoa; 
De volta ao Main exiba no terminal o nome alterado; 
    
#### Demo II: 
```
static void TrocarNome(Pessoa p1, string nomeNovo)
{
    p1.Nome = nomeNovo;
}
    public static void Main() 
    {
        Pessoa p1 = new Pessoa(); 
        p1.Nome = "Bruno";
        p1.Idade = 27;
        p1.Documento = "1234";

        TrocarNome(p1, "Tavares");
        WriteLine($"O novo nome é: {p1.Nome}");
    }
```
//
//
//

#### Atribuindo valores e referências.

Aula prática, com o VSCode... anotações feitas aqui:* Nem sempre levar em consideração oque é mostrado no ícone da chave na stack, pois nem sempre o item é interpretado como reference type.

```
    public static void Main()
    {
        Pessoa p1 = new Pessoa();
        p1.Nome = "Bruno";
        p1.Idade = 27;
        p1.Documento = "1234";
        
        Pessoa p2 = p1.Clone();
        
        new Pessoa();
        p2.Documento = p1.Documento;
        p2.Nome = p1.Nome;
        p2.Idade = p1.Idade; 
```

[Realiza a cópia do conteúdo. Uma nova referência para uma nova instância, para deixar o código mais limpo, pode se criar um método adequado para manter o código limpo.]

```
        TrocarNome(p1, "Tavares");
        
        WriteLine($@"
        O nome de p1 é: {p1.Nome}
        O nome de p2 é: {p2.Nome}
         ");
    } 
```

*<Métodos: Substitui o código comentado acima. Quando você invoca uma cópia e não um reference type*

```
    public Pessoa Clone ()
    {
        return new Pessoa()
        {
        Documento = this.Documento,
        Idade = this.Idade,
        Nome = this.Nome
        };
    } 
``` 

- Criando um arquivo novo com nome de "StructPessoa.cs" 

```  
    public struct StructPessoa
    {
        public int Idade {get; set;}
        public string Nome {get; set;}
        public string Documento {get; set;}
    } 
```    
- Adicione um novo trocar como: 
- Cada chamado de métodos são stacks diferentes, então não tem problemas de terem o mesmo nome, pois o escopo delas está fechado dentro daquela stack 
```    
    static void TrocarNome(StructPessoa P1, string nomeNovo)
    {
        p1.Nome = nomeNovo;
    } 
``` 
- Código novo ao final do código no code. 
- Não se altera devido a realizar uma cópia, interpretada como struct pela IDE. 
- Trabalhando só com a stack, ele nem chega na HEAP. 
- Para o uso de ambas depende do modelo que será realizado. 
- Com muitos pontos, um reference type é melhor. 
 ```
    public static void Main ()
    {
        StructPessoa p1 = new StructPessoa
        {
            Documento = "123",
            Idade = 30,
            Nome = "Ricardo"
        };
        
        var p2 = p1;
        
        TrocarNome(p2, "Nome novo João");
        
        WriteLine($@"
            Nome do p1 {p1.Nome}
            Nome do p2 {p2.Nome}
        ");
        
    }
```
