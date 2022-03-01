# ComandosDocker<br />
Alguns comandos principais para iniciar a aplicação docker<br />

docker stop [id]<br />
docker run --help<br />
docker run -it ubuntu<br />
docker pull ubuntu<br />
docker run ubuntu<br />
apt update<br />
apt upgrade -y<br />
apt -y install <br />

Procedimento de instalação https://docs.docker.com/engine/install/ubuntu/

*****************************************************

Instalando as imagens - (UBUNTO)<br />
Siga os passos. <br />
- docker pull ubuntu<br />

A mensagem que deve aparecer é a seguinte.<br />

seu_usuario@DESKTOP-AVGRC2I:~$ docker pull ubuntu<br />
Using default tag: latest<br />
latest: Pulling from library/ubuntu<br />
08c01a0ec47e: Pull complete<br />
Digest: sha256:669e010b58baf5beb2836b253c1fd57655555f0d1dbcb834f7c07a4dc93f474be<br />
Status: Downloaded newer image for ubuntu:latest<br />
docker.io/library/ubuntu:latest<br />

*****************************************************

Agora digite o comando.<br />
docker run ubuntu<br />

Siga com o comendo: sudo docker pull hello-world, a mensagem que deve aparecer é a seguinte.<br />
Seu_Ususario @DESKTOP-AVGRC2I:~$ sudo docker pull hello-world<br />
[sudo] password for seu_usuario:<br />
Using default tag: latest<br />
latest: Pulling from library/hello-world<br />
Digest: sha256:97a37U3H4JD9075586364637373838e597b2209f49a<br />
Status: Image is up to date for hello-world:latest<br />
docker.io/library/hello-world:latest<br />

Em seguida, para confirmar que houve o download da imagem, digite, docker images.<br />
a mensagem que deve ser exibida é a seguinte.<br />
seu_usuario@DESKTOP-AVGRC2I:~$ docker images<br />
REPOSITORY               TAG         IMAGE ID       CREATED        SIZE<br />
hello-world              latest      feb5d9fea6a5   5 months ago   13.3kB<br />

********************************************************
Executando a imagem hello-world:<br />
docker run hello-world<br />

Será exibida a seguinte mensagem:<br />
docker run hello-world<br />

Hello from Docker!<br />
This message shows that your installation appears to be working correctly.<br />

To generate this message, Docker took the following steps:<br />
 1. The Docker client contacted the Docker daemon.<br />
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)<br />
 3. The Docker daemon created a new container from that image which runs the<br />
    executable that produces the output you are currently reading.<br />
 4. The Docker daemon streamed that output to the Docker client, which sent it<br />
    to your terminal.<br />

To try something more ambitious, you can run an Ubuntu container with:<br />
 $ docker run -it ubuntu bash<br />

Share images, automate workflows, and more with a free Docker ID:<br />
 https://hub.docker.com/<br />

For more examples and ideas, visit:<br />
 https://docs.docker.com/get-started/<br />

Isto significa que a imagem que foi realizada o download esta rodando.<br />


*******************************************************************************

Para visualizar os contêineres basta usar o comando
docker ps.<br />
 docker ps
CONTAINER ID   IMAGE                           COMMAND        CREATED      STATUS          PORTS            <br />                                                                                NAMES
7a5e78108ae8   portainer/portainer-ce:2.11.1   "/portainer"   3 days ago   Up 41 minutes   0.0.0.0:8000->8888/tcp, <br />
:::8000->8888/tcp, 0.0.0.0:9443->9444/tcp, :::9444->9444/tcp, 9999/tcp   portainer<br />

Esta mensagem aparece quando o comendo docker ps é usado.<br />

*********************************************************************************

docker ps -a<br />
informa quais containeres foram usando recentemente<br />

*********************************************************************************

Use: docker run it- ubuntu para iniciar o sistema operacional.<br />

seu_usuario@DESKTOP-AVGRC2I:~$ docker run -it ubuntu<br />
root@7e83fc7d43d3:/# ls -l<br />
total 48
lrwxrwxrwx   1 root root    7 Jan 13 16:47 bin -> usr/bin<br />
drwxr-xr-x   2 root root 4096 Apr 15  2020 boot<br />
drwxr-xr-x   5 root root  360 Mar  1 15:23 dev<br />
drwxr-xr-x   1 root root 4096 Mar  1 15:23 etc<br />
drwxr-xr-x   2 root root 4096 Apr 15  2020 home<br />
lrwxrwxrwx   1 root root    7 Jan 13 16:47 lib -> usr/lib
lrwxrwxrwx   1 root root    9 Jan 13 16:47 lib32 -> usr/lib32
lrwxrwxrwx   1 root root    9 Jan 13 16:47 lib64 -> usr/lib64
lrwxrwxrwx   1 root root   10 Jan 13 16:47 libx32 -> usr/libx32
drwxr-xr-x   2 root root 4096 Jan 13 16:47 media<br />
drwxr-xr-x   2 root root 4096 Jan 13 16:47 mnt<br />
drwxr-xr-x   2 root root 4096 Jan 13 16:47 opt<br />
dr-xr-xr-x 183 root root    0 Mar  1 15:23 proc<br />
drwx------   2 root root 4096 Jan 13 16:50 root<br />
drwxr-xr-x   5 root root 4096 Jan 13 16:50 run<br />
lrwxrwxrwx   1 root root    8 Jan 13 16:47 sbin -> usr/sbin
drwxr-xr-x   2 root root 4096 Jan 13 16:47 srv<br />
dr-xr-xr-x  11 root root    0 Mar  1 15:23 sys<br />
drwxrwxrwt   2 root root 4096 Jan 13 16:50 tmp<br />
drwxr-xr-x  13 root root 4096 Jan 13 16:47 usr<br />
drwxr-xr-x  11 root root 4096 Jan 13 16:50 var<br />
root@7e83fc7d43d3:/#<br />

****************************************************************

docker run -dti ubuntu<br />
Este comendo executa a applicação em background<br />
Você pode sair do conteineres mas ele continuarar em execução.<br />

****************************************************************

Após o comando anterior usei o comendo docker PS, para listar minhas imagens, ao verificar o ID de uma imagem ubunto, <br />
eu selecionei apenas o 3 primeiro digitos do seu id, sendo ele 334, seguido do argumento /bin/bash <br />
seu_usuario@DESKTOP-AVGRC2I:~$ docker exec -it 334 /bin/bash <br />
root@334e22716115:/# <br />


****************************************************************


Após o comando anterior, basta usar o comando LS para verificar que você já esta dentro do container <br />

****************************************************************

https://www.hostinger.com.br/tutoriais/install-docker-ubuntu

docker attach – Anexar padrões locais de entrada, saída e streams de erro para um container em execução<br />
docker build – Construir uma imagem a partir de um Dockerfile<br />
docker builder – Gerenciar builds<br />
docker checkpoint – Gerenciar checkpoints<br />
docker commit – Criar uma nova imagem a partir das mudanças de um container<br />
docker config – Gerenciar configurações do Docker<br />
docker container – Gerenciar containers<br />
docker context – Gerenciar contextos<br />
docker cp – Coipar arquivos/pastas entre um container e um sistema de arquivos local<br />
docker create – Criar um novo container<br />
docker diff – Inspecionar mudanças de arquivos ou diretórios no sistema de arquivos de um container<br />
docker events – Obter eventos em tempo real do servidor<br />
docker exec – Executar um comando num container em execução<br />
docker export – Exportar o arquivo de sistemas de um container como arquivo tar <br />
docker history – Exibir o histórico de uma imagem<br />
docker image – Gerenciar images <br />
docker images – Listar images<br />
docker import – Importar os conteúdos de uma tarball para criar uma imagem de arquivo de sistema<br />
docker info – Exibir informações de todo o sistema<br />
docker inspect – Retornar informações de baixo nível sobre os objetos do Docker<br />
docker kill – Finalizar um ou mais containers em execução<br />
docker load – Carregar uma imagem a partir de um arquivo tar ou STDIN<br />
docker login – Fazer login para um registro do Docker <br />
docker logout – Fazer logout de um registro do Docker<br />
docker logs – Obter os registros de um container<br />
docker manifest – Gerenciar os manifestos de imagens e manifestos de listas do Docker<br />
docker network – Gerenciar redes<br />
docker node – Gerenciar Swarm nodes<br />
docker pause – Pausar todos os processos dentro de um ou mais containers<br />
docker plugin – Gerenciar plugins<br />
docker port – Listar mapeamentos de portas ou mapeamentos específicos para um container<br />
docker ps – Listar containers<br />
docker pull – Puxar uma imagem ou repositório a partir de um registro<br />
docker push – Empurrar uma imagem ou repositório para um registro<br />
docker rename – Renomear um container<br />
docker restart – Reiniciar um ou mais containers <br />
docker rm – Remover um ou mais containers <br />
docker rmi – Remover uma ou mais images <br />
docker run – Executar um comando num novo container <br />
docker save – Salvar uma ou mais imagens num arquivo tar (enviado para STDOUT por padrão) <br />
docker search – Buscar o Hub do Docker por mais imagens <br />
docker secret – Gerenciar segredos do Docker <br />
docker service – Gerenciar serviços <br />
docker stack – Gerenciar stacks <br />
docker start – Iniciar um ou mais containers parados <br />
docker stats – Exibir uma transmissão ao vivo das estatísticas de uso de container(s) <br />
docker stop – Finalizar um ou mais containers que estão sendo executados <br />
docker swarm – Gerenciar Swarm <br />
docker system – Gerenciar Docker <br />
docker tag – Criar uma tag TARGET_IMAGE que se refere a SOURCE_IMAGE <br />
docker top – Exibir os processos em execução num container <br />
docker trust – Gerenciar o trust nas imagens Docker <br />
docker unpause – Despausar todos os processos dentro de um ou mais containers <br />
docker update – Atualizar configuração de um ou mais containers <br />
docker version – Mostrar informações de versão do Docker <br />
docker volume – Gerenciar volumes <br />
docker wait – Bloquear até um ou mais containers pararem, e então imprimir seus códigos de saída <br />




