# Aula 01:
  - O Kubernetes é utilizado para criar um cluster
  - Um cluster é um ou mais container para disponibilizar que forma uma aplicação
  - Dentro do cluster as maquinas se conhecem mas existe um "gerente"
  - O gerente se chama master (mestre em português)
  - No cluster também tem um ou mais node para rodar a aplicação
  - O Kubernetes tem o seu foco em aplicações que rodam usando containers
  - O Kubernetes é uma plataforma open-source desenvolvida pela Google

# Aula 02:

  - Para testar o kubernetes localmente usa-se o minikube
  - Para rodar o cluster usa-se minikube start
  - Para parar o cluster: minikube stop
  - Para limpar e apagar: minikube delete
  - Minikube usa alguma virtualização por baixo dos panos como virtualbox ou vmware
  - Para controlar o cluster usa-se kubectl
  - O menor objeto de deploy é o Pod
  - Um Pod é o objeto que define como rodar o container (image, network, volumes, ports)
  - Um Pod sozinho não garante o estado desejado
  - O comando kubectl create é usado para criar um Pod ou Deployment no cluster
  - O Deployment se baseia no Pod e garante o estado desejado
  - Para receber infos sobre os Pods ou Deployments usamos kubectl get pods ou kubectl get deploymentP


# Aula 03:

  - O comando kubectl describe pods mostra vários detalhes sobre os pods como o endereço IP
  - O comando minikube dashboard mostra o dashboard do nosso cluster
  - Podemos escalar o quantidade de Pods facilmente pelo dashboard
  - Cada Pod possui o seu IP
  - O objeto Service abstrai o acesso ao Deployment
  - O Service funciona como um balanceador de carga entre os Pods
  - O Service é definido separadamente
  - O Service seleciona os Pods através do elemento selector
  - Para descobrir o IP e a porta do serviço podemos utilizar o comando: minikube service service-aplicacao --url

# Aula 04:

  - Para trabalhar com volumes no Kubernetes existe o objeto StatefulSet
  - Um StatefulSet também usa um Pod por baixo dos panos.
  - Um StatefulSet pode definir um volume (e existem vários tipos)
  - Um StatfulSet garante, através do volume, que os dados serão mantidos mesmo se o POD for reiniciado
  - Para o volume funcionar devemos configurar a permissão (PersistentVolumeClaim)
  - As configuração da permissão fica dentro de um arquivo separado junto à definição do tamanho do volume (storage)