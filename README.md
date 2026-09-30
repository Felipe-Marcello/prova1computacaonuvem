Nome: Felipe Antonio Souza Marcello
RA: ae242abd3179e74703bd

## O que fiz

Executei uma página web em um contêiner Docker chamado pedidos.
Usei a imagem nginx:alpine e a porta 8084 do ambiente.

##Verificação do contêiner

root@ubuntu:~$ docker ps 
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS                                     NAMES
baed99c0fafe   nginx:alpine   "/docker-entrypoint.…"   49 seconds ago   Up 48 seconds   0.0.0.0:8084->80/tcp, [::]:8084->80/tcp   pedidos

##Teste da página

root@ubuntu:~$ curl http://localhost:8084
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Pedidos</title>
</head>
<body>
<h1>Pedidos em funcionamento</h1>
</body>
</html>

##Explicação 
Uma imagem é um modelo estático e somente leitura que contém o código, as bibliotecas e as configurações, enquanto um contêiner é a instância em execução dessa imagem.
