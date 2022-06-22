### Tipos por Referência & Tipos por Valor. 
    
    Objetivo do Curso: Entender a diferença entre utilizar variáveis por referência e valor, value type, será fundamental para entender como o compilador executa o código que você escrever. Ou seja, sem entender esse conceito fundamental um desenvolvedor terá muitos problemas para descobrir bugs. 

    Conceitos / Prática
    Palavra chave: ref
    Palavra chave: ref Struct
    Comparação por Valor e por Referência
    Garbage Collector

    Reference Types: Value Types!

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
