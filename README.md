# Projeto de Newsletter Odontológica da OdontoPrev
https://whimsical.com/odontoletter-F1HE1xFVV6mmu3qtj6noCv



![image](https://github.com/user-attachments/assets/7dd6bbe5-3912-4ee6-8269-8a5b52718771)



## Visão Geral do Projeto

Este projeto é parte de uma iniciativa da OdontoPrev para melhorar a comunicação com profissionais da área odontológica e clientes. O sistema consiste em uma aplicação web desenvolvida em .NET MVC para gerenciar e enviar newsletters com informações relevantes sobre procedimentos odontológicos, atualizações da empresa e dicas de saúde bucal.

O objetivo principal é manter os assinantes informados sobre as últimas novidades no campo da odontologia, promover boas práticas de higiene bucal e divulgar serviços e promoções da OdontoPrev.

## Arquitetura do Projeto

Este projeto segue os princípios da Clean Architecture para manter o código desacoplado e facilitar a manutenção e escalabilidade. A estrutura do projeto é dividida nas seguintes camadas:

### Camadas da Aplicação

1. **Apresentação**
   - Controllers: RedatorController, NewsletterController
   - Views (não implementadas neste projeto MVC API)

2. **Aplicação**
   - Services: RedatorService, NewsletterService
   - ViewModels: RedatorViewModel, NewsletterViewModel, LoginViewModel

3. **Domínio**
   - Models: Redator, Newsletter

4. **Infraestrutura**
   - Data: NewsletterDbContext
   - Repositories: RedatorRepository, NewsletterRepository

## Definição do Projeto

### Objetivo do Projeto
O objetivo deste projeto é criar uma plataforma para gerenciar e enviar newsletters odontológicas. Esta plataforma servirá como um canal de comunicação eficiente entre a OdontoPrev e seus assinantes, incluindo profissionais de odontologia e clientes.

### Escopo
Este projeto abrange o desenvolvimento de uma aplicação web utilizando .NET MVC para gerenciar assinantes, criar e enviar newsletters. O escopo inclui:

1. Sistema de autenticação para redatores
2. Interface de administração para criar, editar e enviar newsletters
3. Gerenciamento de assinantes
4. API para possível integração futura com outros sistemas

### Requisitos Funcionais
1. Autenticação de redatores
   - Login seguro para redatores
   - Gerenciamento de perfis de redator

2. Gerenciamento de Newsletters
   - Criação de novas newsletters
   - Edição de newsletters existentes
   - Envio de newsletters para assinantes
   - Visualização do histórico de newsletters enviadas

3. Gerenciamento de Assinantes
   - Adição e remoção de assinantes
   - Segmentação de assinantes por categorias (ex: dentistas, clientes)

4. API RESTful
   - Endpoints para gerenciar newsletters e assinantes

### Requisitos Não Funcionais
1. Segurança
   - Utilização de HTTPS para todas as comunicações
   - Armazenamento seguro de senhas (hashing)
   - Proteção contra ataques comuns (SQL Injection, XSS, CSRF)

2. Desempenho
   - Capacidade de enviar newsletters para pelo menos 10.000 assinantes em menos de 1 hora
   - Tempo de resposta da API inferior a 500ms para 95% das requisições

3. Usabilidade
   - Interface responsiva para acesso via desktop e dispositivos móveis
   - Design intuitivo para facilitar a criação e envio de newsletters

4. Manutenibilidade
   - Código bem documentado
   - Utilização de padrões de projeto para facilitar futuras expansões

5. Compatibilidade
   - Suporte aos principais navegadores (Chrome, Firefox, Safari, Edge)
   - Newsletters compatíveis com os principais clientes de e-mail

6. Escalabilidade
   - Arquitetura que permita fácil escalabilidade horizontal para suportar aumento no número de assinantes

## Detalhes das Classes Principais

### Redator
- Propriedades:
  - Id
  - Nome
  - Email
  - Username
  - PasswordHash
  - Especializacao
  - DataCadastro
  - Ativo

### Newsletter
- Propriedades:
  - Id
  - Titulo
  - Conteudo
  - DataCriacao
  - DataEnvio
  - RedatorId
  - Enviada

### RedatorController
- Métodos:
  - POST: Login
  - GET: GetAllRedatores
  - POST: CreateRedator
  - PUT: UpdateRedator
  - DELETE: DeleteRedator

### NewsletterController
- Métodos:
  - GET: GetNewsletters
  - GET: GetNewsletter
  - POST: CreateNewsletter
  - PUT: UpdateNewsletter
  - DELETE: DeleteNewsletter
  - POST: SendNewsletter

## Fluxo de Funcionamento

1. **Redator**
   - Acessa a aplicação
   - Realiza login
   - Cria ou edita newsletters
   - Envia newsletters para assinantes

2. **Sistema**
   - Gerencia assinantes
   - Processa o envio de newsletters
   - Mantém histórico de newsletters enviadas

3. **Assinante**
   - Recebe newsletters por e-mail
   - Pode se inscrever ou cancelar a inscrição (através de um link na newsletter)

## Tecnologias Utilizadas
- .NET 8.0 ou superior
- ASP.NET Core MVC
- Entity Framework Core
- Banco de dados Oracle
- JWT para autenticação

# Integrantes

[Liste aqui os nomes dos integrantes do projeto]

### Turma: 2TDSPS
Bia Silva 
Pedro henrique S araujo 553801

