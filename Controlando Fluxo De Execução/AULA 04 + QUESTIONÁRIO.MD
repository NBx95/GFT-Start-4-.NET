### AULA 4: PULANDO COM BREAK E CONTINUE. 
#### *Caso utilize um valor 0 para encerrar a aplicação pode se colocar o "break", e caso queira que a aplicação conitnue "continue". 
#### "Entender como pula uma determinada condição de um bloco de laço de repetição"*

//

#### EXEMPLO AULA QUATRO: 
- class: Program.cs

```
    using System; 

    namespace aulaQuatro 
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
                        break;
                        }
                        else
                        {
                            Console.WriteLine("O valor informado é: " + valor);
                            continue;
                        }
                } while(condicao == true);
            }
        }
    }
    
[abra o terminal dentro do VSCode, e execute o comando "dotnet run" para que a aplicação seja iniciada.]
```



#### QUESTIONÁRIO FINAL.

Para que serve o comando WHILE: *Executa um bloco de repetição caso a instrução passada por parâmetro seja verdadeira.*

Qual a função do comando SWITCH: *Executa uma comparação de valores para executar determinado bloco de código através de uma condição.*

Como funciona o CONTINUE: *Faz pular determinado trecho de instrução de laço e continua a execução.* 

Como funciona o FOREACH: *Percorre uma lista de variáveis, fazendo um laço por cada item.*

Como funciona o comando de repetição DO: *Faz uma execução inicial de um laço de repetição, e em seguida valida com o comando WHILE.*

Código com trexo errado, qual seria esse erro: 
int valor;
        Console.WriteLine("Digite um número");
        valor1 = Console.ReadLine(); 
R: *Faltou converter para inteiro o valor que será passado no Console.ReadLine(), pois a tipagem padrão de estrada é string.*

Para que serve o Console.ReadLine(): *Faz a captura da informação passada pelo Console.*

Qual a finalidade do comando IF: *Especifica uma condição passada por parâmetro para que possa executar determinado bloco de código.* 

Para que serve o Console.WriteLine(): *Grava os dados de entrada para que possa ser apresentado no Console.*

Qual a função do BREAK: *Faz interromper o loop da execução durante a aplicação.*
