# DOCKER-QA

<p align="center">
  <img src="docker-qa.png" alt="animated" />
</p>

:white_check_mark: 
:white_check_mark: comandos docker utilizados
:white_check_mark: subir aplicação no docker
:white_check_mark: container customizado

### 💻 Configurações

- 🎯 Ubuntu 22.04 [LTS] 
- 🎯 [Docker Engine](https://docs.docker.com/engine/install/ubuntu/)
- 🎯 [NGINX](https://github.com/nginxinc) 
- 🎯 VS Code
  
## 💾 Instalação do Docker no Ubuntu e Criação do Container

[Docker Engine](https://docs.docker.com/engine/install/ubuntu/)
[Permissão de SUPERUSER no Docker](https://docs.docker.com/engine/install/linux-postinstall/)

## 🎲 Comandos:

Comandos para criar o container:
```
docker run -d -p 8080:80 -v [caminho-projeto-local]:[caminho-arquivo-html-docker]/html nginx
```
Lista containers iniciados:
```
docker ps
```
Lista containers iniciados e parados:
```
docker ps -a
```
Lista as imagens:
```
docker images
```
Inicia container:
```
docker start [id]
```
Para container:
```
docker stop [id]
```
Remove container:
```
docker rm [id]
```
Executa docker dentro do container:
```
docker exec -it [id] bash
```

## 🎲 Comandos dentro do container:
Lista pastas do sistema
```
ls -l
```
Atualiza sistema
```
apt update
```
Instala ferramenta
```
apt install [nome_ferramenta]
```
Caminhar pelas pastas
```
cd [caminho]
```

## 🚀 Subir Aplicação no Docker

- colar o repositório app dentro do repositório local
```
docker run -d -p 8081:80 -v $(pwd)/app:/[caminho-arquivo-html-docker]/html nginx
```

## 🚀 Customizar Nome do Container 

- customizar nome:
```
docker run -d -p 8081:80 -v $(pwd)/app:[caminho-arquivo-html-docker]/html --name [nome-container] nginx
```

## 🚀 Empacotar a Aplicação
- cria arquivo Dockerfile dentro da aplicação
- cria a imagem:
```
docker build -t [nome-imagem]
``` 
cria o container apontando para a imagem criada: 
```
docker run -d -p 8082:80 --name [nome-container] [nome-imagem]
```

## ❓ Outros Comandos

🟢 Comandos vim
  - i: entrar no modo de edição
  - esc: sai do modo de edição
  - shift + ":" + wq! : salva arquivo editado

<b>Lourena Ohara</b>

