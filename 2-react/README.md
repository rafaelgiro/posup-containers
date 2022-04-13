# Exercício 2 - React

Criar uma imagem Docker para um site utilizando qualquer framework/biblioteca frontend e que disponibilize o site em alguma porta http. Entregar a URL da imagem, Dockerfile, e comando de execução da imagem

## Executando

```bash
docker build -t cra:dev .
docker run --name cra -d -p 3000:3000 cra:dev
```

Acesse: [http://localhost:3000](http://localhost:3000)

**[Dockerhub](https://hub.docker.com/repository/docker/rafaelgiro/cra)**
