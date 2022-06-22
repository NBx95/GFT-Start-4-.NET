#### Estudos sobre DotNet / Studies On DotNet

Resultado dos ensinamentos apresentado no bootcamp sobre .NET dentro da webDio.

- Passado, Presente e Futuro do .Net: A Microsoft iniciou nos anos 70 criando linguagens de programação: Basic. Já nos anos 80, surge o DOS, que foi utilizado como OS padrão para computadores IBM. Nos próximos anos a Microsoft atua fortemente na criação do OS Windows. 

1997: A Microsoft tentou consolidar as ferramentas de desenvolvimento (IDEs e runtimes)
Visual Studio 97: {Visual Basic 5, Visual FoxPro 5, C++5 e J++(J java da Microsoft)}. 
Lancamento do Visual Studio 6: Visual Basic 6, Visual FoxPro 6, C++6 e J++ =6 

1999: Scott Guthrie criou uma ferramenta web com Java, e a chamou de ASP+ (depois chamou ASP Next e depois ASPX) Jason Zandler ajudou na criação de um commom runtime para VB e C++ (CLR = Cammom Language Runtime) 
Ainda em 99, Java ia bem! Então a Sun Microsystem fez um acordo para a Microsoft não mexer mais com Java Com isso Anders Hejlsber começou a trabalhar na criação do C#. 

2000: A Microsoft lança o novo ambiente de desenvolvimento .NET 1.0 - inicialmente chamado de Next Generation Windows Services (NGWS). Miguel de Icaza começa a trabalhar no projeto Mono, uma reimplementação black box do .NET, open source e multiplataforma. 

2002: lançamento do Visual Studio .NET com C# 1.0 conhecido como 22 linguagens, 1 plataforma: C#.net, C++.net, VB.net, J#.net entre outras. 

2003: lançamento do .NET 1.1 com o Visual Studio 2003, trabalham em melhorias na CLR para lançar a CLR2. 

((Cada código com seu compilador convertendo para linguagem intermediaria sendo interpretada pela CLR para linguagem de máquina (binário))

2005: Lançamento do .NET 2.0 com C# 2.0 no Visual Studio 2005. A Microsoft começa a atingir seu objetivo inicial, inclusive evoluindo na web, realizado nesse período o ASP .Net web forms, com plataforma consolidada, sendo mais difundida, em paralelo com o próprio Java OpenSource na epóca. 

2007 - 08: Lançamento do .NET 3.5 com C# 3.0 no Visual Studio 2008, com Silverlight, WPF e WCF. A Microsoft contrata então um time de pessoas que tinham uma pegada open source e começam a atuar na criação do ASP.NET MVC, surgindo assim os primeiros assuntos sobre o Windows Azure. 

2010: Lançament do .NET 4.0 com C# 4.0 no Visual Studio 2010, também com F#. Microsoft lança comercialmente o Windows Azure. Anders Hejlsberg começa a trabalhar no 'Typescript'. 

2011: Miguel de Icaza inicia a Xamarin, basicamente ele desenvolvia em C# aplicativos que rodam em Android e iOS. 

2012: Lançamento do .NET 4.5 com C# 5.0 no Visual Studio 2012 e o lançamento do 'Typescript'

2013: Lançamento do .NET 4.5.1 no VisualStudio 2013, inicio do Roslyn, um novo compilador para C# e VB.NET. A Microsoft continua atuando mais na frente JS e aumenta também a incorporação de ferramentas open source ao ambiente, Já temos aqui o ASP.NET mais consolidado com MVC,Web API e SignaIR. 
 
2014: Satya Nadella se torna CEO da Microsoft e direciona o foco da empresa para Cloud. Criação do .NET Foundation para gestão de projetos open source. Windows Azure passa a se chamar Microsoft Azure. É introduzido o conceito do ASP.NET vNext, posteriormente chamado de ASP.NET Core. 

2015: Lançamento do .NET 4.6 com C# 6.0 no Visual Studio 2015. Lançou no mercado Visual Studio Code. 

2016: Microsoft adquire a Xamarin e adiciona o produto como parte de sua stack .NET e projetos open source. Lançamento do Visual Studio for MAC. (até então era unicamente compativél com Sistemas Operacionais Windows.) No mesmo ano, pelo final do ano surge o .NET Core 1.0 - Totalmente novo, open source e multiplataforma! 

2017: Lançamento do .NET Framework 4.7 com C# 7.0 no Visual Studio 2017. Lançamento do .NET Core 2.0 com C# 7.0 no Visual Studio 2017, Visual Studio Code ou Visual Studio for Mac 2017. 

2019: Lançamento do .NET Framework 4.8 com C# 7.3 no Visual Studio 2019. Lançamento do .NET Core 3.0 com C# 8.0 no Visual Studio 2019, Visual Studio Code ou Visual Studio for Mac 2019. 

2020: .NET Framework está pronto na versão 4.8! E deixa de ser evoluído - junto com ele WCF e ASP.NET Webforms, Previsto o lançamento do .NET 5, o .NET juntara tudo o que há de melhor em todas suas versões anteriores..!!!

- O que é, Como e Onde Usar .NET ?

É uma infraestrutura criada para desenvolvimento de software criada pela Microsoft. Uma aplicação .NET é desenvolvida para e rodar em uma das seguintes implementações do .NET: 
- .NET Core.
- .NET Framework.
- Mono.
- Universal Windows Plataform (UWP). 

.NET Standard Library, One library to rule them all. É básicamente um contrato, para implentar uma versão X do Standard vc precisa ter o mesmo range de funcionalidades implementadas funcionando. Cada versão do .NET implementam X funcionalidades. Isso garante que todos funcionaldiades funcionem em acordo com cada uma das versões. 

Cada implementação inclui um ou mais .NET Runtimes (ambiente de execução)
- .NET Core: CoreCLR e CoreRT.
- .Net Framework: CLR. 
- Mono: Mono Runtime.
- UWP: .NET Native. 

Atualmente a Microsoft desenvolve e suporta 3 linguagens para .NET: C#, F# e VB. 

- Quem usa .NET ?
vidalink, licks, casas bahia, saraiva, seguros unimed, br, guarani, takeda, ctc, rodobens, pressganey, techs, unimed (paulistana, brasil, fesp).
hub finTech, marabraz, aacd, são francisco, GOL, Azul, MinervaFoods, WalmartArgentina, Linx, Itau, stackOverFlow e Microsoft.

===========================================================================================================================================================

### Ambiente de Desenvolvimento. 

1: Praparando o Ambiente = Instalação básica do Windows, usando na aula a versão 3.1.4 para os exemplos realizados junto com o VSCode. 

2: Conhecendo a CLI do .NET = comandos e flags. 
* dotnet --help 
(mostra a versão, o tipo de usubilidade, o caminho da aplicação entre outros argumentos) 
Mostra as opções que você pode usar junto do 'dotnet' estude a documentação a fundo após a aula.
* dotnet new --help. (estudar as maneiras de se criar aplicações via CLI.

3: Criando uma aplicação console.
É uma aplicação que será executada via terminal. 
*dotnet new console -h* (ver as opção que são dadas)
*dotnet new console -n DigitalInnovationOne* 

*dentro da pasta que você quer abrir dentro do visualCode use o comando = code .*

{ 
(dentro do .NET no VSCode)
Projeto .NET
output gera um exe. 
qual framework
} 

dotnet build. ele gera os executaveis, dependencias. Unico arquivo que de fato está criado é o Program.CS com o método main. 

*dotnet run* executa o código feito de acordo com o salvo no VSCode.
*dotnet build (caminho do arquivo)* para atualizar sem estar na pasta exata.
*dotnet run -p (diretório que se encontra o arquivo)*
