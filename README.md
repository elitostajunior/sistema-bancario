# Documentação do Projeto Back-end - Sistema Bancário

## Introdução
Este é um projeto back-end que simula um sistema bancário. Ele foi desenvolvido usando a linguagem TypeScript e a biblioteca Express para criar uma API REST. O sistema possui funcionalidades básicas de criar conta, obter todas as contas e realizar uma validação de idade durante o processo de criação de uma nova conta.

## Estrutura do Projeto
O projeto é organizado em três arquivos:

1. `index.ts`: Contém o código da aplicação Express e as rotas para criar um usuário e obter todos os usuários.
2. `types.ts`: Define os tipos `Transaction` e `Account`, que representam transações bancárias e informações da conta do usuário, respectivamente.
3. `accounts.ts`: Exporta o array `accounts`, que armazena todas as contas de usuários criadas no sistema.

## Funcionalidades

### 1. Criar Conta
Endpoint: `POST /users/create`

Descrição: Permite cadastrar um novo usuário no sistema, criando uma conta bancária.

Parâmetros (Corpo da Requisição):
- `name`: Nome do usuário (string).
- `CPF`: Número do CPF do usuário (string).
- `dateOfBirthAsString`: Data de nascimento do usuário no formato "DD/MM/AAAA" (string).

Resposta de Sucesso (Status 201):
- "Conta criada com sucesso!"

Resposta de Erro (Status 400 ou 406):
- Caso ocorra algum erro de validação (por exemplo, o usuário ter menos de 18 anos): Mensagem de erro detalhando o problema.

### 2. Pegar Todas as Contas
Endpoint: `GET /users/all`

Descrição: Retorna todas as contas de usuários existentes no sistema.

Resposta de Sucesso (Status 200):
- Array contendo todas as contas de usuários.

Resposta de Erro (Status 404):
- "Nenhuma conta encontrada" (caso não haja contas cadastradas no sistema).

## Execução do Projeto
Para executar o projeto, você deve ter o Node.js instalado. Em seguida, siga os passos abaixo:

1. Instale as dependências do projeto:
```
npm install express cors
```

2. Execute o projeto:
```
npm start
```

O servidor estará rodando na porta 3003. Agora você pode enviar requisições para as rotas `POST /users/create` e `GET /users/all` utilizando um cliente HTTP, como o Postman ou o curl.

## Considerações Finais
Este projeto é uma versão inicial e pode ser aprimorado com mais funcionalidades e validações de acordo com as necessidades do sistema bancário simulado. Sinta-se à vontade para expandir e melhorar o código conforme necessário.

