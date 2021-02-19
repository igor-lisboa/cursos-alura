* https://cursos.alura.com.br/course/docker-swarm-cluster-container
# Aula 1
* O Docker Swarm é um orquestrador
* O Docker Swarm é capaz de alocar e reiniciar containers de maneira automática
* Como criar máquinas já provisionadas para utilizar o Docker com a Docker Machine utilizando comando `docker-machine create`
* Um cluster é um conjunto de máquinas dividindo poder computacional
* Como criar um cluster utilizando o Docker Swarm utilizando o comando `docker swarm init`
# Aula 2
* Que nós *workers* são responsáveis por executar containers
* Comandos de leitura e visualização de nós, como o docker node ls
* Comandos que leem ou alteram o estado do swarm só podem ser executados em nós *managers*
* O comando `docker container run` sobe containers em escopo local e o `docker service create` cria serviços em escopo do swarm
* Tarefas são instâncias de serviços
* Portas são compartilhadas entre nós do swarm e são acessíveis a partir de qualquer nó graças ao *routing mesh*
# Aula 3
* Que nós *managers* são primariamente responsáveis pela orquestração do swarm
* A importância e como realizar o backup do swarm
* Que podemos ter mais de um nó *manager* no swarm
* A importância do *Leader* dentro do swarm
* Como é feita a eleição de um novo *Leader* em caso de falhas
* Os requisitos para funcionamento do *RAFT*
# Aula 4
* Como readicionar um manager posterior a uma falha
* Restringir nós de executarem quaisquer serviços utilizando o `docker node update --availability drain`
* Restringir serviços de serem executados em determinados nós utilizando o `docker service update --constraint-add`

# Aula 5
* Serviços replicados rodam em um ou mais nós do swarm
* Serviços globais rodam em todos os nós do swarm
* Nós *managers* por padrão trabalham como *workers*
* Serviços como monitoramento e segurança são bons exemplos de serviços globais
* Como definir o modo que o serviço será criado utilizando a flag `--mode` no momento da criação do serviço

# Aula 6
* A rede *ingress* é a padrão criada junto com nosso swarm
* O driver *overlay* é utilizado para a comunicação entre nós em diferentes hosts
* Como criar nossas próprias redes com o driver overlay utilizando o comando `docker network create -d overlay`
* Redes overlays criadas manualmente (User-Defined Overlay) permitem a comunicação entre serviços por seus nomes (Service Discovery)
* As redes criadas com o driver overlay são listadas de maneira lazy para workers

# Aula 7
* O *docker-compose.yml* também pode ser utilizado para serviços de um swarm
* Novas instruções a partir da versão 3, como *deploy* e suas instruções internas
* Uma *stack* é uma pilha de serviços trabalhando em conjunto
* Como criar e remover nossa própria stack utilizando o comando `docker stack`