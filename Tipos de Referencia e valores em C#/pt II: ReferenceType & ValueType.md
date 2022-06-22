 #### Strings = Uma reference type, 
 ##### Com um comportamento diferentes das demais. É feita cópias quando se chega no método e após o fim todos são apagados.
            
 Cria uma Console application com uma variável do tipo string e atribui o valor a esta variável; 
 Crie também uma método void que receba essa variável e altere esse valor;
 No Main escreve através do terminal o valor a ser alterado;
            
 - Código do VS Code: *exemploUM*
 ```
static void exemploUM
    {
        StructPessoa p1 = new StructPessoa
        {
            Documento = "1234",
            Idade = 30,
            Nome = "Ricardo"
        };
        
        var p2 = p1;
        
        p1 = TrocarNome(p1, "João");
        
        WriteLine($@"
        Nome do p1 {p1.Nome}
        Nome do p2 {p2.Nome}
        ");
    }
    static void TrocarNome(string nome, string nomeNovo)
    {
        nome = nomeNovo;
    }
    public static void Main()
    {
        string nome = "Bruno";
        TrocarNome(nome, "Nobru");
        WriteLine($"O novo nome é {nome}");
    }
``` 
//
//
//

#### Arrays (reference type(porem será colocado um value type dentro da array)).
    
Criar uma Console application com uma variável do tipo array de int para armazenar os números pares de 0 a 8;
Crie um método void que receba essa variável e altere o conteúdo desse array para que nele fique armazenado o próximo número inteiro ímpar de cada elemento; (troca de par para ímpar)
No Main escreva no terminal todos os números desse array;

- Código do VS Code: *exemploDOIS*

```    
    static void exemploDOIS()
    {
        string nome = "Bruno";
        trocarNome(nome, "Nobru");
        WriteLine($"O novo nome é {nome}");
    }
    static void mudaParaImpar(int[] pares)
    {
        for (int i > 0; i < pares.Length; i++)
        {
            pares[i] = pares[i] + 1;
        }
    }
    public static void Main()
    {
        int[] pares = new int[]{0, 2, 4, 6, 8};
        mudarParaImpar(pares);
        WriteLine($"Os ímpares {string.Join(",", pares)}");
    }
    
*Join : Junta uma array.*
``` 

//
//
//

#### Desenvolvendo um Algoritmo.
Criar uma Console application para encontrar um número inteiro em um array;
Criar uma console application para encontrar uma pessoa em uma Lista de pessoas; 
[pode ser trocada para procurar um serviço rodando, porta aberta, url de site entre outras coisas].    
 
- Código do VS Code: *exemploTRES*
 
 ``` 
    static int encontrarNumero(int[] numeros, int numero)
    {
        for(int i = 0; i < numeros.Length; i++)
        {
            if(numeros[i] = número)
                return i;
        }
        return -1;
    }
    
    public static void Main()
    {
        int[] numero = new int[] {0,2,4,6,8};
        WriteLine($"Digite o número que gostaria de encontrar");
        var numero = int.Parse(ReadLine());
        var idxEncontrado = encontrarNumero(numeros, numero);
        
        if(idxEncontrado => 0)
        {
        WriteLine($"O número digitado está na posição {idxEncontrado}");
        }
        else
        {
        WriteLine("O número digitado não foi encontrado");
        }
    }
```     
//
#### EXEMPLO TRÊS pt II:
//
``` 
    static bool encontrarPessoa(List<Pessoa> pessoas, Pessoa pessoa)
    {
        foreach (var item in pessoas)
        {
            if(item.Nome = pessoa.Nome)
            {
                return true;
            }
        }
        return false;
    }
    
    public static void Main()
    {
        List<Pessoa> pessoas = new List<Pessoa>()
        {
            new Pessoa(){Nome = "Bruno"},
            new Pessoa(){Nome = "Nobru"},
            new Pessoa(){Nome = "Onurb"},
            new Pessoa(){Nome = "Norbu"},
            new Pessoa(){Nome = "Urbon"},
        };
        WriteLine("Digite a pessoa que gostaria de Localizar:");
        var nome = ReadLine();
        var pessoa = new Pessoa(){Nome = nome};
        var encontrado = encontrarPessoa(pessoas, pessoa);
        if (encontrado)
        {
            WriteLine("Pessoa localizada!");
        }
        else
        {
            WriteLine("Pessoa não localizada!");
        }
    } 
```

#### EXEMPLO COM O STRUCT PESSOA:

- Código do VS Code: *exemploQUATRO*

``` 
    static bool encontrarPessoa(List<StructPessoa> pessoas, StructPessoa pessoa)
    {
        foreach (var item in pessoas)
        {
            if(item.Equals(pessoa))
            {
                return true;
            }
        }
        return false;
    }
    public static void Main()
    {
        List<StructPessoa> pessoas = new List<StructPessoa>()
        {
            new StructPessoa(){Nome = "Bruno"},
            new StructPessoa(){Nome = "Nobru"},
            new StructPessoa(){Nome = "Onurb"},
            new StructPessoa(){Nome = "Norbu"},
            new StructPessoa(){Nome = "Urbon"},
        };
        WriteLine("Digite a pessoa que gostaria de Localizar:");
        var nome = ReadLine();
        var pessoa = new StructPessoa(){Nome = nome};
        var encontrado = encontrarPessoa(pessoas, pessoa);
        if (encontrado)
        {
            WriteLine("Pessoa localizada!");
        }
        else
        {
            WriteLine("Pessoa não localizada!");
        }
    }

``` 
//

### Aprendendo a utilizar a palavra chave "ref keywords" 

- Tipos por Referência e Valor: 
- Utilização: O "ref" indica que o conteúdo de determinada variável acessada, será acessado por referência. E pode ser usada em 4 situações... Uma palavra chave que pode ser colocada em alguns pontos do código, e esta palavra chave, muda o comportamento do próprio compilador. 
    
   1º Na declaração dos parâmetros do método e na chamada do método.
(podemos colocar a palavra "ref" em determinado parâmetro, de entrada... no caso de entrada e na hora que for chamado o método, teremos que também indicar o “palavra ref".)
    
   2º Na declaração do retorno do método.
(Pode ser usada quando um método estiver retornando, indo na declaração o ref.)

   3º No corpo do método para receber um retorno com ref.
(No momento da chamada de um método que retorna um "ref", tendo que declarar a variável que vai receber esse retorno, ela vai ter a anotação da "ref" antes da declaração do tipo. Ele sempre vai antes da tipagem normal.)
    
   4º Na declaração de uma Struct.
(Quando declarar um Struct, você pode informar que essa Struct terá um "ref" na frente e que isso irá de fato alterar coisas dentro dessa Struct.)

//

#### DEMOS: Explicar com ref no parâmetro de entrada o mesmo que feito no *exemploUm*

//
- Código do VS Code: *exemploCINCO*:
        
``` 
using static System.Console;
class aulaCINCO
{
    static void Adicionar20(ref int a)
    {
        a +=20;
    }
    static void Main()
    {
        int a = 5;
        Adicionar20(ref a);
        WriteLine($"O valor de a é {a}"!);
    }
}
```
//

#### Criando uma Array de String:
//
- Código do VS Code: *exemploSEIS*:

``` 
    static void AlterarNome(string[] nomes, string nome, string nomeNovo)
    {
        for (int i = 0; i < nomes.Length; i++)
        {
            if(nomes[i] == nome)
            {
                nomes[i] = nomeNovo;
            }
        }
    }
    
    static void Main()
    {
        var nomes = new string[]{"José", "Maria", "Alice", "Pedro"};
        
        WriteLine($@"A Lista de nomes é: 
            {string.Join(", \n",nomes)}
        ");
        
        WriteLine("Digite o nome a ser trocado");
        var nome = ReadLine();
        
        WriteLine("Digite o nome novo");
        var nomeNovo = ReadLine();
        
        AlterarNome(nomes, nome, nomeNovo);
        
        WriteLine($@"A Lista de nomes Alterada é:
            {string.Join(", \n",nomes)}
        ");
    }
``` 

//

#### Desenvolvendo o Projeto::
//
- Código do VS Code: *exemploSETE*:

```
static ref string LocalizarNome(string[] nomes, string nome)
{
    for (int i = 0; i < nomes.Length; i++)
    {
        if(nomes[i] == nome)
            return ref nome[i];
    }
    throw new Exception("Nome não encontrado");
}

static void Main()
{
    var nomes = new string[]{"José", "Maria", "Alice", "Pedro"};
    
    WriteLine($@"A Lista de nomes é: 
        {string.Join(", \n",nomes)}
    ");
    
    WriteLine("Digite o nome a ser trocado");
    var nome = ReadLine();
    
    WriteLine("Digite o nome novo");
    var nomeNovo = ReadLine();
    
    ref var nomeAchado = ref LocalizarNome(nomes, nome); 
    
    if(string.IsNullOrWriteSpace(nomeAchado))
    {
        nomesAchado = nomeNovo; 
        
        WriteLine($@"A Lista de nomes Alterada é:
            {string.Join(", \n",nomes)}
        ");
    }
    else
    {
        WriteLine("Nomes não encontrado!");
    }
}
``` 
        
#### Descobrindo o que é um ref struct (valueType)

"ref struct": Serve para assegurar que a struct ficará na stack e nunca irá para a Heap. 
Não tem o processo de boxing, que seria pegar esse valueType que é Struct e o próprio compilador ir alocar o mesmo na HEAP, por necessidade de tratar o mesmo como objeto/referência. 
Neste caso queremos garantir que o Struct vai ta sempre na Stack; 

- Ref struct "não pode": 
- Ser elemento tipado de um array
- Ser o tipo em campo em uma classe ou não-ref struct
- Implementar interfaces
- Ser convertida para Object e nem para ValueType
- Ser usada em métodos assíncronos

*Então, quando usar:* Quando for necessário garantir que a instância da struct não irá acessar a Heap: 

Quando criada uma struct sem a palavra "ref", eu informo que quero um struct, um objeto mais simples para ser criado na stack. 
Dependendo da onde ele será usado/aplicado por ser um ValueType, quando mandado aquele método como ref, acaba sofrendo o unboxing (encapsulado para Heap) para ser tratado como referência. 
- Quando for usar tipos do C# que são "ref struct", como o caso do ref struct Span: 

Existe um objeto novo no C# que se chama Span, esse sendo herdeiro de um ValueType, mas possui notação de "ref" se for criado um struct para agrupar objetos do tipo "spam" não se pode realizar isso com um struct comum, precisará ser um ref por natureza. 


#### EXEMPLO PRÁTICO: 
##### Deve-se construir uma ref struct e tentar utilizá-la em uma classe. 
###### Busque tentar usar um Span em uma não-ref struct. 

``` 
* +1 arquivo: objetos.cs* 

    public class Pessoa
    {
    public int Idade {get; set;}
    public string Nome { get; set;}
    public Endereco EnderecoPessoa {get; set;}
    }
    
    public struct Endereco
    {
    public int Numero {get; set;}
    public string Logradouro {get; set;}
    public string CEP {get; set;}
    public string Cidade {get; set;}
    }
``` 

#### C# Program.cs 

```
    using static System.Console; 
    
    Pessoa p1 = new Pessoa ();
    p1.Nome = "Bruno";
    p1.Idade = "27";
    p1. EnderecoPessoa = new Endereco()
    {
        Logradouro = "Rua Randon", 
        CEP = "11920-000",
        Número = "59",
        Cidade = "Iguape",
    };
 
    WriteLine("Fim");
```    
