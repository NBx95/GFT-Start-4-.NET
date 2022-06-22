### *"O dev será capaz de aprender as estruturas de condição e repetição bem como receber e capturar informações do usuário pelo console."* 

#### PERCURSO:       
- AULA 1: Capturando entradas do usuário pelo console.
- AULA 2: Comando condicional, IF e SWITCH.
- AULA 3: Comando de repetição, FOR, FOREACH, DO e WHILE.
- AULA 4: Pulando com BREAK e CONTINUE. 

#### PRÉ-REQUISITOS:        
- SDK .NET5.
- Visual Studio Code.
- Conhecimentos Sintaxe C#. 
    
### AULA 1: CAPTURANDO ENTRADAS DO USUÁRIO PELO CONSOLE.# 
#### *"Entender como capturar as informações enviadas pelo usuário e fazer cálculos a partir dessas informações."*####

```     
    classe: Program.cs

    using System; 
    
    namespace aulaUm
    { 
        class Program
        {
            static void Main(string[] args)
            {
                int valorUm;
                int valorDois; 
                int total;
                
                Console.WriteLine("Digite o primeiro valor: ");
                valorUm = int.Parse(Console.Readline());
                Console.WriteLine("O primeiro valor é: " + valorUm);
                Console.WriteLine("Digite o segundo valor: ");  
                valorDois = int.Parde(Console.ReadLine());
                Console.WriteLine("O segundo valor é: " + valorDois);
                
                total = valorUm + valorDois; 
                Console.WriteLine("A soma dos valores é: " + total);
                
            }
        }
    }
    
    [abra o terminal dentro do VSCode, e execute o comando "dotnet run" para que a aplicação seja iniciada.]
``` 

