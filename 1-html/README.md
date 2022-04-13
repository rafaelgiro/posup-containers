# Exercício 1 - HTML com NGINX

Criar uma imagem Docker para um site estático que retorne uma simples página HTML, e publicar a imagem no Dockerhub. Entregar a URL da imagem e o Dockerfile

## Executando

```bash
docker build -t html-nginx .
docker run --name html -d -p 8080:80 html-nginx
```

Acesse: [http://localhost:8080](http://localhost:8080)

**[Dockerhub](https://hub.docker.com/r/rafaelgiro/html-nginx)**
