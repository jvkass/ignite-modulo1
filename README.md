# ignite-modulo1
Fundamentos do Node e conceitos de API REST

# Conceitos Node.js

Arquitetura baseada em Event Loop
- call stack

Single - Thread

Non-blocking I\O

Modulos proprios
- http
- dns
- fs
- buffer
- ...

# Event Loop

Toda vida que uma função entrar na Pilha de chamada(Call Stack), o Event Loop fica escutanto uma requisição por vez e repassando essas Req para uma thread, por padrão há 4 threads, o que pode ser aumentado conforme o desempenho da maquina. Observando que o que entrar por ultimo vai sair primeiro da fila.

# Gerenciadores de Pacotes

Os principais gerenciadores atualmente são o NPM e Yarn, eles são utilizados para instalar bibliotecas externas e disponibilizar bibliotecas proprias. Em questão de velocidade de download o yarn é mais rápido.

# API REST

- Application Programming Interface

- Conjunto de especificações de possíveis interações entre aplicações 

- Documentação para desenvolvedor

# REST

- Representation State Transfer

- Modelo de arquitetura

- 6 regras

# Regras 

1 - Client-Server (Relação cliente e servidor esta definida de forma direta onde não a necessidade de conhecimento de ambas as partes para utilização dos serviços)

2 - Stateless (Cliente pode fazer quantas requisições quiser mas o servidor não é responsável por guardar estados da mesma, sendo necessário informar todas as informações para que a mesma seja processada)

3 - Cache (A aplicação tem que ser construida de forma que possua o cache para eventuais necessidades futura)

4 - Interface Uniforme
    - Identificação dos recursos
        -- http://enderecoservidor.com.br/products
        -- http://enderecoservidor.com.br/clients

    - Representação dos recursos
    - Mensagens auto-descritivas
    - HATEOAS (Utilizado para retorna links dentro da Requisição)

5 - Camadas (Aplicação é para ser construida em camadas)

6 - Código Sob Demanda

# Metodos de Requisições 

- GET - Leitura
- POST - Criação
- PUT - Atualização
- DELETE - Deleção
- PATCH - Atualização Parcial

# HTTP Codes

- 1XX: Informativo - a solicitação foi aceita ou o processo continua em andamento.

- 2XX: Confirmação
    - 200 - Requisição bem sucedida
    -- 201 - Created - Geralmente usado para POST após uma inserção

- 3XX: Redirecionamento 
    -- 301 - Moved Permanently
    -- 302 - Moved

- 4XX: Erro do Cliente
    -- 400 - Bad Request 
    -- 401 - Unauthorized
    -- 403 - Forbidden
    -- 404 - Not Found
    -- 422 - Unprocessable Entity

- 5XX: Erro no servidor - o servidor falhou ao concluir a solicitação.
    -- 500 - Internal Server Error 
    -- 502 - Bad Gateway

# Parâmetros das Requisições

- Header Params 
    authority: app.rocketseat.com.br
    method: GET
    path: /api/journey-nodes
    scheme: https
    referer: https://app.rocketseat.com.br/node/

- Query Params
    -- Chave
    -- Valor
    -- Separação

- Route Params
    -- http://enderecoservidor.com.br/v1/users/{id}

- Body Params
  {
      "name": "Joao",
      "username:"Vitor"
  }   

# Boas Práticas API Rest

- A utilização correta dos métodos HTTP
- A utilização correta dos status no retorno das respostas
- Padrão de nomenclatura 
    -- Busca de usuários - GET
        --- http://enderecoservidor.com.br/v1/users
    -- Busca de usuário por id - GET
        --- http://enderecoservidor.com.br/v1/users/1
    -- Busca de endereço do usuário - GET
        --- http://enderecoservidor.com.br/v1/users/1/adress
    -- Deleção de um usuário - DELETE
        --- http://enderecoservidor.com.br/v1/users/1
    -- Atualização do status do usuário - PATCH
        --- http://enderecoservidor.com.br/v1/users/1/status


