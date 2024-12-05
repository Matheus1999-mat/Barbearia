# Projeto Barbearia: API BackEnd Completa em C#

## Sobre o Projeto
Estamos criando uma API para ajudar na gestão de uma barbearia, focando em agendamentos, controle de estoque e gestão de clientes. Utilizamos a **Clean Architecture** para garantir que o código seja organizado e fácil de manter, além de documentar tudo de forma clara para que qualquer pessoa possa usar e entender.

## Como o Projeto Está Organizado
Para facilitar o desenvolvimento e a manutenção, organizamos o código em diferentes pastas:

- **Properties**
- **Controllers**
- **Application**
- **Domain**
- **Infrastructure**

### Arquitetura e Padrões
Estamos seguindo o modelo Hexagonal, que separa bem as responsabilidades do sistema. A organização do código é feita nas seguintes áreas:

- **Core/Domain**: Regras de negócio.
- **Application**: Lógica da aplicação.
- **Infrastructure**: Infraestrutura, como o banco de dados.


## Link de download
O link de download está localizado no arquivo Barbearia - api -download.txt

## O que Estamos Desenvolvendo
O objetivo é criar uma API robusta usando **ASP.NET CORE**. Vamos implementar padrões de projeto como **Mediator**, **Repository** e **Notification**. O foco é atender às necessidades específicas da barbearia.

### Funcionalidades
- **Agendamentos**: Permitir que os clientes agendem, atualizem ou cancelem horários. Antes disso, é necessário cadastrar um cliente e um profissional.
- **Gestão de Clientes**: Facilitar o cadastro, edição e remoção de clientes.
- **Controle de profissionais**: Realizar o cadastro, busca, atualização e remoção de profissionais.
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

- **Visual Studio**: é a IDE que pode ser usada. Nesse caso, pode-se instalar a versão Community. O link de download é esse: https://visualstudio.microsoft.com/pt-br/vs/community/
- **SQL Server**: é o banco de dados utilizado no projeto.
 

## Como executar o projeto:
1. Faça o download do projeto;

2. Após isso, navegue entre as pastas do projeto, até encontrar um arquivo chamado **Sistema de barbearia.sln**. Dê um duplo clique;

3. Após isso, na parte lateral direita do Visual Studio, dentro da solução "Sistema de barbearia", procure o arquivo appsettings.json;
![appsettings](https://github.com/user-attachments/assets/2a33715c-9114-4cfa-8bac-3d9f5c63d684)


4. Após isso, abra esse arquivo appsettings.json. No item "ConnectionSettings", faça a configuração da string de conexão ao banco de dados, colocando as respectivas credenciais do seu SQL Server;
![string](https://github.com/user-attachments/assets/4e6ac8b8-12cf-42ce-bd1f-3cc331f06cfe)

5. Após isso, na parte superior do Visual Studio, porcure a aba Compilação, em seguida clique em Recompilar solução;
![Captura de tela 2024-12-05 092827](https://github.com/user-attachments/assets/adef81c5-f0bc-40a0-92c2-edfac5090840)

6. Após isso, na parte superior do Visual Studio, procure a aba Ferramentas. Em seguida, o item "Gerenciador de Pacotes do Nuget". Após isso, o item "Console do gerenciador de pacotes";
![ferramentas](https://github.com/user-attachments/assets/892063c6-606b-45be-868f-d804253f16da)


7. Após seguir o passo 6, na linha de comando, digite **cd "Sistema de barbearia"** e dê enter. Após isso, escreva **cd Infrastructure** e dê enter. Após isso, escreva **cd Migrations** e dê enter;

8. Digite o comando **Update-Database** e dê enter, para executar as migrations. As migrations são comandos que servem para conexão ao banco de dados, para que seja possível fazer as operações necessárias;

9. Execute o projeto;

10. Uma interface do swagger deve aparecer.

## Estrutura de Código
- **Controllers**: Contêm as rotas e endpoints da API.
- **Data**: Inclui contextos e acesso ao banco de dados.
- **DTO (Data Transfer Objects)**: Utilizados para transferir dados entre camadas.
- **Migrations**: Histórico e controle das alterações no banco de dados.
- **Domain**: Representações das entidades do sistema.
- **Application**: Lógica de negócios e operações sobre as entidades.

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

![diagrama](https://github.com/user-attachments/assets/6493a5b5-cf7f-40e3-8722-8f299d853800)



**Relacionamento**: 1 para N com Agendamento. O campo ClienteID de Agendamento será chave estrangeira, que referencia ClienteID de Cliente. 
Isso significa que, antes de cadastrar um agendamento, é necessário cadastrar um cliente.

**Relacionamento**: 1 para N com Agendamento. O campo ProfissionalID de Profissional será chave estrangeira, que referencia ProfissionalID de Profissional. 
Isso significa que, antes de cadastrar um agendamento, também é necessário cadastrar um profissional responsável pelo agendamento.

**Relacionamentos**: após cadastrar um cliente e um profissional, pode-se cadastrar um agendamento. 


