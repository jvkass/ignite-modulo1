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

