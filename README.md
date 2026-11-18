# Simulado-pratico-integrado-de-computacao-em-nuvem

Instituição: Anhanguera
Disciplica: Computação em nuvem
Professora: Simone Tatiane do Canto
Data: 18/11/2026
Aluno: Erick da Silva Rodrigues

Parte 1 Fundamentos da Computação em nuvem

1- Fundamentos da Computação em nuvem

questão 1 - Qual é a diferença entre Iaas e Saas? Cite um exemplo de cada modelo.

Resposta: Iaas é a Infraestrutura como serviço, é quando uma empresa ou equipe precisa de um serviço que ofereça o hardwere para eles enquanto a parte de softwere e sistema operacional fica por parte do cliente, já o Saas Softwere como serviço é quando é oferecido a plataforma completa ao cliente com hardware e sistemas inclusos, o cliente normalmente contrata esse serviço quando ele não quer desenvolver nada só acessar e utilizar como a netflix por exemplo.

questão 2 - Qual a principal diferença de maquina virtual e container?

Resposta: A maquina virtual é quando uma pessoa sacrifica parte da capacidade fisica do computador para ter outro sistema dentro da sua própria maquina, exemplificando seria como emular um sistema (criar uma maquina virtual), já o container permite você armazenar na nuvem um código ou um sistema inteiro dentro de um container onde você pode acessar de qualquer local caso queira, coisa que é impossivel com a maquina virtual que se limita há apenas o computador em que a maquina virtual está instalada.

Parte 2 execução da Aplicação docker
Código Evidencia 1:
cat> index.html <<EOF
> Erick da Silva Rodrigues EOF
> EOF
root@controlplane:~$ docker run -d --name pedidos -p 8090 nginx:alpine 
Unable to find image 'nginx:alpine' locally
alpine: Pulling from library/nginx
881fc932939e: Pull complete 
77a3bfea78f5: Pull complete 
04c3905a997c: Pull complete 
7cb374baf968: Pull complete 
4c8c172c6586: Pull complete 
1dc588c89da1: Pull complete 
61d8f4c85a74: Pull complete 
c4f3d97811f6: Pull complete 
Digest: sha256:0563c36f94a6d3ec3584161b77859f740f7e20b4853f52c796a864ce6908e8ea
Status: Downloaded newer image for nginx:alpine
b9827c95cf930edeff635b0ecdb82933672158ff881c969d286c14171f39efde
root@controlplane:~$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED         STATUS         PORTS                                                   NAMES
b9827c95cf93   nginx:alpine   "/docker-entrypoint.…"   5 seconds ago   Up 4 seconds   80/tcp, 0.0.0.0:32768->8090/tcp, [::]:32768->8090/tcp   pedidos

Evidencia 2
curl http://localhost:8090
curl: (7) Failed to connect to localhost port 8090 after 0 ms: Couldn't connect to server
A falha ocorreu pois não consegui me conectar com o servidor.

Parte 6 adiantamento:
Questão 1:Qual a diferença entre uma Imagem docker e um container em execução?

Resposta: A Imagem docker é oque vai ser guardado dentro do container servindo de referencia.

Questão 2: qual a função de um deployment no kubernetes?

Resposta: Criar pods, e exibir eles.

Questão 3: Oque acontece quando você excluí um pod? porque isso ocorreu?

Resposta: um dos três pods criados é apagado sobrando somente 2, podendo ser recuperado repetindo o comando "kubectl get pods"


Parte 7 Conclusão:

Aprendi como funciona e como criar um container utilizando docker, se tratando de uma forma de armazenar um código, podendo acessa-lo posteriormente com outra maquina, aprendi a diferença de container e maquina virtual, aprendi a como armazenar uma mensagem no docker po´rem infelizmente não consegui executa-la
