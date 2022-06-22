### AULA 2: COMANDOS CONDICIONAIS, IF & SWITCH.
#### *"Entender como funciona as condicionais em uma aplicação de diversas formas e soluções."* 
    
#### EXEMPLO I:
- classe: Program.cs
```    
    using System; 
    
    namespace aulaDois
    { 
        class Program
        { 
            static void Main(string[] args)
            { 
                int idade; 
                
                Console.WriteLine("Digite sua idade: "); 
                idade = int.Parse(Console.ReadLine()); 
                
                    if(idade >= 18)
                    {
                        Console.WriteLine("Você possui 18 anos");
                    }
                    else
                    {
                        Console.WriteLine("Você não possui 18 anos");
                    }
            }
        }
    }

[abra o terminal dentro do VSCode, e execute o comando "dotnet run" para que a aplicação seja iniciada.]
```


#### EXEMPLO II:
###UTILIZAÇÃO DO IF / ELSE IF / ELSE
- classe: Program.cs
```
    using System; 
    
    namespace aulaDois
    { 
        class Program
        { 
            static void Main(string[] args)
            {
                int mes;
                
                Console.WriteLine("Digite um número do mês");
                mes = int.Parse(Console.ReadLine());
                if(mes == 1)
                {
                    Console.WriteLine("Janeiro");
                }
                else if(mes == 2)
                {
                    Console.WriteLine("Fevereiro");
                }
                else if(mes == 3)
                {
                    Console.WriteLine("Março");
                }
                else if(mes == 4)
                {
                    Console.WriteLine("Abril");
                }
                else if(mes == 5)
                {
                    Console.WriteLine("Maio");
                }
                else if(mes == 6)
                {
                    Console.WriteLine("Junho");
                }
                else if(mes == 7)
                {
                    Console.WriteLine("Julho");
                }
                else if(mes == 8)
                {
                    Console.WriteLine("Agosto");
                }
                else if(mes == 9)
                {
                    Console.WriteLine("Setembro");
                }
                else if(mes == 10)
                {
                    Console.WriteLine("Outubro");
                }
                else if(mes == 11)
                {
                    Console.WriteLine("Novembro");
                }
                else if(mes == 12)
                {
                    Console.WriteLine("Dezembro");
                }
                else
                {
                    Console.WriteLine("Mês não encontrado");
                }
                
            }
        }
    }

[abra o terminal dentro do VSCode, e execute o comando "dotnet run" para que a aplicação seja iniciada.]
```

#### EXEMPLO III:
#####UTILIZAÇÃO DO SWITCH CASE AULA DOIS:

```
                switch (mes);
                {
                    case 1:
                    Console.WriteLine("Janeiro");
                    break;
                    
                    case 2:
                    Console.WriteLine("Fevereiro");
                    break;
                    
                    case 3:
                    Console.WriteLine("Março");
                    break;
                    
                    case 4:
                    Console.WriteLine("Abril");
                    break;
                    
                    case 5:
                    Console.WriteLine("Maio");
                    break;
                    
                    case 6:
                    Console.WriteLine("Junho");
                    break;
                    
                    case 7:
                    Console.WriteLine("Julho");
                    break;
                    
                    case 8:
                    Console.WriteLine("Agosto");
                    break;
                    
                    case 9:
                    Console.WriteLine("Setembro");
                    break;
                    
                    case 10:
                    Console.WriteLine("Outubro");
                    break;
                    
                    case 11:
                    Console.WriteLine("Novembro");
                    break;
                    
                    case 12:
                    Console.WriteLine("Dezembro");
                    break;
                }

[abra o terminal dentro do VSCode, e execute o comando "dotnet run" para que a aplicação seja iniciada.]

``` 
