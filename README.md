# Contexto

Este projeto foi feito do zero como teste de processo seletivo. O enunciado, com as especificações do que foi pedido, encontra-se no arquivo Teste_BancoMaster.txt.

# Tecnologias

Foram usados o .Net 8 e o Angular 19. Para rodar os projetos, é necessário possuir ao menos os seguintes itens instalados:
- Runtime do Microsoft.AspNetCore.App 8
- Node nas seguintes versões: ^18.19.1 || ^20.11.1 || ^22.0.0

# Como rodar

## API

Na mesma pasta onde está o arquivo BestRouteMasterBankTest.sln, execute no terminal de sua preferência o comando `dotnet run --project ./BestRoute/BestRoute.csproj`. 

## Cliente

Na mesma pasta onde está o arquivo package.json, execute no terminal de sua preferência os comandos `npm install` e `npm start`.

# Decisões

## Arquitetura

O projeto foi feito utilizando uma arquitetura simples de MVC, pois foi o bastante para o escopo pedido. Utilizar arquiteturas avançadas para um projeto tão simples seria um *overengineering*. Ainda assim, procurou-se organizar o código em uma devida estrutura de pastas, as separações de responsabilidade básicas foram respeitadas. Foi utilizado o padrão *repositório* como demonstração, para não ficar demasiadamente simplista, apesar de também ter sido desnecessário frente ao tamanho e escopo do projeto.

## Persistência

O projeto utiliza o banco *InMemory* do Entity Framework, configurado com Code First, o que torna trivial trocar para qualquer outro banco suportado, como MS Sql Server, ou PostgreSQL. Neste caso, deverá ser trocado o provider e geradas e aplicadas as migrations.

## Front-end

Devido ao foco no back-end, e ao curto tempo de desenvolvimento, o front-end foi feito limitado à interação mais básica possível para efetivar um CRUD. Propositalmente, não foram dadas as devidas atenções ao layout, mensagem e tratamento de erros, componentização, etc.