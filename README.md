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

Os principais gerenciadores atualmente são o NPM e Yarn, eles são utilizados para instalar bibliotecas externas e disponibilizar bibliotecas proprias. Em questão de velocidade de download o yarn é mais rápido 