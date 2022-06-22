### Aprendendo a comparar Valores e Referências: 
    
##### C# program.cs 

```
    using static System.Console;
    
    Numero a = new Numero(2);
    Numero b = new Numero(2);
    
    if (a == b) [overloads devido o comportamento da classe, sobre seus parametros de referencia seja por valor ou padrão]
    {
        WriteLine($"a e b são iguais");
    }
    else
    {
        WriteLine("a e b são diferentes");
    }
    
    class Numero
    {
        public int N {get; set;}
    }
    public Numero (int n)
    {
        N = n;
    } 
```    

##### EXPLICANDO: Agora que aprendemos a diferença entre ValueTypes e ReferenceTypes, vamos entender o funcionamento do CLR ao comparar esses tipos.
    
*ValueTypes: instância = a instância.* 
*ReferenceTypes: referência = a referência. *

#### Garbage Collector.GC: "Tipos por referência e valor"

*GC - Definição. Suporte para a criação e destruição de objetos na HEAP.*
    
#### Vantagens - GC: 
- Segurança. 
- Programador não precisa se preocupar com a liberação de memória. 
- Nem com sobrescrita de memória em uso. 

#### Desvantagens - GC: 
- Performance. 
- Observabilidade. 

#### Arquitetura - GC: 
- O GC é dividido em 3 Gerações. 
*Geração 1*: Objetos de ciclo de vida curto. 
*Geração 2*: Buffer da alternancia entre Gen 1 e Gen 3. 
*Geração 3*: Objetos com longo ciclo de vida em especial objetos criados como "static". 
        
##### REVIEW:
      
- O que são reference e value types e seu comportamento. 
- Demos sobre alocação na stack e na heap. 
- Boas práticas na criação de classes, struct. 
- A palavra chave ref em parâmetros de entrada. 
- A palavra chave ref no retorno de métodos e na atribuição de variáveis. 
- Comportamento do CLR ao comparar value e reference types. 
- O que é e como é o funcionamento básico do GarbageCollector. 
