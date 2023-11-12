## Primeiros passos com docker

### Instalação

Primeiro, faça a atualização de seus pacotes:

        $ sudo apt update

Instale o docker com apt-get:

        $ sudo apt install docker.io


Por fim, verifique se o Docker está instalado corretamente:

        $ sudo docker run hello-world


### Comandos uteis 


Usado para baixar imagens de contêineres do Docker Hub ou de outro registro de contêineres para o seu ambiente local. 

        docker pull nome_da_imagem[:tag]

Criar sua imagem para que contenha sua aplicação.

        docker build -t python-test .

A opção '-t' permite que você defina o nome de sua imagem.

Para rodar aplicação através do docker

        docker run python-test

Listar suas imagens.

        $ docker image ls


Excluir uma imagem específica.

        $ docker image rm [nome da imagem]

Listar todos os contêineres existentes (em execução ou não).

        $ docker ps -a


Parar um contêiner específico.

        $ docker stop [nome do contêiner]

Parar todos os contêineres em execução.

        $ docker stop $(docker ps -a -q)

Exibir os logs (registros) de um contêiner.

        $ docker logs [nome do contêiner]

Excluir um contêiner específico (que não estiver em execução).

        $ docker rm [nome do contêiner]

Excluir todos os contêineres (apenas se estiverem parados).

        $ docker rm $(docker ps -a -q)