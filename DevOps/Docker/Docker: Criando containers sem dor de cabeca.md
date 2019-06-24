# Aula 01, aprendemos

- conheceu a ideia de virtualização,
- entendeu o conceito de containers,
- descobriu o que é o Docker e suas principais tecnologias,
- instalou o Docker no sistema operacional,
- e o testou através de uma imagem Hello, World, que foi baixada do Docker Hub

# Aula 02, aprendemos

- Comandos básicos do Docker para podermos baixar imagens e interagir com o container.
- Imagens do Docker possuem um sistema de arquivos em camadas (Layered File System) e os benefícios dessa abordagem principalmente para o download de novas imagens.
- Imagens são Read-Only sempre (apenas para leitura)
- Containers representam uma instância de uma imagem
- Como imagens são Read-Only os containers criam nova camada (layer) para guardar as alterações
- O comando Docker run e as possibilidades de execução de um container

# Aula 03, aprendemos

- Que Container são voláteis, isso é, ao remover um, removemos os dados juntos
- Para deixar os dados persistente devemos usar Volumes
- Que volumes salvos não ficam no container e sim no Docker Host
- Como criar um ambiente de execução node.js

# Aula 04, aprendemos

- A entender o papel do arquivo DockerFile para criar imagens.
  - O Dockerfile define os comandos para executar instalações complexas e com características específicas.
- Vimos os principais comandos como FROM, MAINTAINER, COPY, WORKDIR, RUN, EXPOSE e ENTRYPOINT
- A subir uma imagem criada através de um Dockerfile para o Docker Hub e disponibilizar para os desenvolvedores

## Lembrando também:

- as imagens são read-only sempre
- um container é uma instância de uma imagem
- para guardar as alterações a docker engine cria uma nova layer em cima da última layer da imagem

# Aula 05, aprendemos

- Que imagens criadas pelo Docker acessam a mesma rede, porém apenas através de IP.
- Ao criar uma rede é possível realizar a comunicação entre os containers através do seu nome.
- Que durante a criação de uma rede precisamos indicar qual driver utilizaremos, geralmente, o driver bridge.
