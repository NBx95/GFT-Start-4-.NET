    
### AULA 3: COMANDOS DE REPETIÇÃO FOR, FOREACH, DO & WHILE.
#### *"Entender a funcionalidade dos comandos de repetição para executar determinado bloco de um código."*

#### EXEMPLO I: UTILIZANDO O BOOLEAN. 
*Verifica uma condição, até que seja validado o valor final correto.*
- class: Program.cs

``` 
    using System; 
    
    namespace aulaTres
    {
        class Program
        { 
            static void Main(string[] args)
            {
                BooLean condicao = true;
                int valor;
                
                while(condicao == true)
                {
                    Console.WriteLine("Digite um valor, 0 para sair: ");
                    valor = int.Parse(Console.ReadLine());
                        if(valor == 0)
                        {
                        Console.WriteLine("Aplicação encerrada");
                        condicao = false;
                        }
                        else
                        {
                            Console.WriteLine("O valor informado é: " + valor);
                        }
                }
            }
        }
    }

[abra o terminal dentro do VSCode, e execute o comando "dotnet run" para que a aplicação seja iniciada.]
``` 
////////////////////////////////////////////////////////////////    

#### EXEMPLO II: UTILIZANDO O DO. 
*Executa o bloco de código até que chegue sua condição final*
- class: Program.cs
```
    using System; 
    
    namespace aulaTres
    {
        class Program
        { 
            static void Main(string[] args)
            {
                BooLean condicao = true;
                int valor;
                
                do {
                    Console.WriteLine("Digite um valor, 0 para sair: ");
                    valor = int.Parse(Console.ReadLine());
                        if(valor == 0)
                        {
                        Console.WriteLine("Aplicação encerrada");
                        condicao = false;
                        }
                        else
                        {
                            Console.WriteLine("O valor informado é: " + valor);
                        }
                } while(condicao == true);
            }
        }
    }
       
[abra o terminal dentro do VSCode, e execute o comando "dotnet run" para que a aplicação seja iniciada.]
```

#### EXEMPLO III: UTILIZANDO O FOR. 
*Analisa e concatena até o indicado.*
- class: Program.cs
```
    using System; 
    
    namespace aulaTres
    {
        class Program
        { 
            static void Main(string[] args)
            {
                int valor; 
                Console.WriteLine("Digite um valor");
                valor = int.Parse(Console.ReadLine());
                
                for(int i = valor; i <= 10; i++)
                {
                    Console.WriteLine(i);
                }
            }
        }
    }

[abra o terminal dentro do VSCode, e execute o comando "dotnet run" para que a aplicação seja iniciada.]
```

#### EXEMPLO IV: UTILIZANDO O FOREACH. 
*Percorre a lista e printa na tela*
- class: Program.cs
``` 
    using System; 
    
    namespace aulaTres
    {
        class Program
        { 
            static void Main(string[] args)
            {
                int[] lista = {1,2,3,4,5};
                
                foreach(int numero in lista)
                {
                    Console.WriteLine("número");
                }
            }
        }
    }

[abra o terminal dentro do VSCode, e execute o comando "dotnet run" para que a aplicação seja iniciada.]
```

