# Projeto Barbearia: API BackEnd Completa em C#

## Sobre o Projeto
Estamos criando uma API para ajudar na gestão de uma barbearia, focando em agendamentos, controle de estoque e gestão de clientes. Utilizamos a **Clean Architecture** para garantir que o código seja organizado e fácil de manter, além de documentar tudo de forma clara para que qualquer pessoa possa usar e entender.

## Como o Projeto Está Organizado
Para facilitar o desenvolvimento e a manutenção, organizamos o código em diferentes pastas:

- **Properties**
- **Controllers**
- **Data**
- **DTO**
- **Migrations**: (Serviço, Agendamento, Cliente, Usuário)
- **Models**
- **Obj**
- **Bin**

### Arquitetura e Padrões
Estamos seguindo o modelo Hexagonal, que separa bem as responsabilidades do sistema. A organização do código é feita nas seguintes áreas:

- **Core/Domain**: Regras de negócio.
- **Application**: Lógica da aplicação.
- **Infrastructure**: Infraestrutura, como o banco de dados.
- **Adapters**: Conexões entre as diferentes partes do sistema.

## O que Estamos Desenvolvendo
O objetivo é criar uma API robusta usando **ASP.NET CORE**. Vamos implementar padrões de projeto como **Mediator**, **Repository** e **Notification**. O foco é atender às necessidades específicas da barbearia.

### Funcionalidades
- **Agendamentos**: Permitir que os clientes agendem, atualizem ou cancelem horários.
- **Gestão de Clientes**: Facilitar o cadastro, edição e remoção de clientes.
- **Controle de Estoque**: Gerenciar produtos e materiais utilizados na barbearia.
- **Segurança**: Usar **JWT** para garantir que só pessoas autorizadas possam acessar a API.
- **Código Seguro**: Implementar técnicas que aumentam a segurança e robustez do sistema.
- **Commands**: Usar requests baseados em Commands para manter o código claro e fácil de manter.

### Ferramentas e Tecnologias
- **ASP.NET CORE**
- **Entity Framework Core** para o banco de dados.
- **Swagger** para testes.


### Melhores Práticas
Estamos adotando boas práticas do mercado, usando teclas de atalho e outras técnicas para aumentar a produtividade, além de documentar tudo de forma que seja fácil de entender e seguir.

## Ferramentas necessárias para executar o projeto
Para utilizar esse projeto, algumas ferramentas são necessárias: 

- **Visual Studio**: é a IDE que pode ser usada. Nesse caso, pode-se instalar a versão Community;
- **Visual Studio Code**: esta é uma outra IDE que também pode ser usada;
- **SQL Server**: é o banco de dados utilizado no projeto.
 

## Instalação e Configuração
1. Clone o repositório para a sua máquina local:
   ```bash
   git clone https://github.com/usuario/barbearia-api.git
   ```

2. Acesse o diretório do projeto:
   ```bash
   cd barbearia-api
   ```

3. Restaure as dependências do projeto:
   ```bash
   dotnet restore
   ```

4. Configure as variáveis de ambiente no arquivo `appsettings.json` para a conexão com o banco de dados e outras configurações necessárias.

5. Execute as migrações para configurar o banco de dados:
   ```bash
   dotnet ef database update
   ```

6. Inicie a aplicação:
   ```bash
   dotnet run
   ```

## Como executar o projeto se for usado o Visual Studio
1. Faça o download do projeto;

2. Após isso, navegue entre as pastas do projeto, até encontrar um arquivo chamado **Sistema de barbearia.sln**. Dê um duplo clique;

3. Após isso, o Visual Studio executará o projeto. Na parte superior, navegue até o item "Ferramentas". Clique em "Gerenciador de pacotes do NuGet". Depois, selecione "Console do gerenciador de pacotes";

4. Na linha de comando, digite **cd "Sistema de barbearia"**. Após isso, escreva **cd Infrastructure**. Após isso, escreva **cd Migrations**;

5. Digite o comando **Update-Database**, para executar as migrations. As migrations são comandos que servem para conexão ao banco de dados, para que seja possível fazer as operações necessárias;

6. Execute o projeto;

7. Uma interface do swagger deve aparecer.

## Estrutura de Código
- **Controllers**: Contêm as rotas e endpoints da API.
- **Data**: Inclui contextos e acesso ao banco de dados.
- **DTO (Data Transfer Objects)**: Utilizados para transferir dados entre camadas.
- **Migrations**: Histórico e controle das alterações no banco de dados.
- **Models**: Representações das entidades do sistema.
- **Services**: Lógica de negócios e operações sobre as entidades.

## Contribuição
Para contribuir com o projeto, siga os passos abaixo:

1. Faça um fork do repositório.
2. Crie uma branch com a sua feature ou correção de bug:
   ```bash
   git checkout -b minha-feature
   ```
3. Commit suas alterações:
   ```bash
   git commit -m 'Adicionei minha feature'
   ```
4. Envie as alterações para o repositório remoto:
   ```bash
   git push origin minha-feature
   ```
5. Abra um Pull Request para revisão.

## Gestão de Issues e Pull Requests
As issues e pull requests serão monitoradas e gerenciadas através do GitHub. Fique atento às boas práticas e aos guias de contribuição descritos no repositório.

## Equipe e Orientação
Esse projeto é parte de uma disciplina de desenvolvimento BackEnd e está sendo desenvolvido por:

- **Matheus Bialuz**
- **Diego Santos**
- **Gabriel Ribas dos Santos**
- **Matheus Freire**

Com a orientação do **Professor Mateus Pereira**.

## Diagrama entidade-relacionamento

![WhatsApp Image 2024-11-26 at 14 52 49](https://github.com/user-attachments/assets/987ab240-4b9d-412f-9df5-2a54085ac55c)

Cliente <-> Agendamento (1:N):

Um cliente pode realizar vários agendamentos.
O campo ClienteID na tabela Agendamento é uma chave estrangeira (FK) que referencia o ClienteID da tabela Cliente.


Serviço <-> Agendamento (N:N):

Um agendamento pode incluir vários serviços, e cada serviço pode estar associado a vários agendamentos.
Este relacionamento provavelmente é implementado por uma tabela intermediária (não representada na imagem) que vincula AgendamentoID e ServicoID.


Usuário (Independente):

A tabela Usuário não possui relações diretas com as outras tabelas no modelo apresentado, indicando que serve apenas para autenticação e gestão do sistema.


