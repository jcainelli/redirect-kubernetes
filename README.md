## Artefatos para crição dos serviços no Kubernetes

#### Dependências:
* Minikube ou Kubernetes

#### Configurações Minikube
1. Para o Minikube buscar imagens locais, alterar o Docker daemon para o do Minikube:    
   >eval $(minikube docker-env)
1. Para voltar ao Docker daemon local:
   >eval $(minikube docker-env -u)

#### Comandos úteis
Comando | Descrição
--------|------------
minikube start | Inicia o Minikube caso esteja parado
minikube dashboard | Dashboard de administração do Minikube
kubectl create/delete -f ./diretorio | Cria/Deleta todos os recursos dentro dos arquivos .yaml da pasta
docker image list | Lista as Imagens Docker
kubectl get svc |Mostra os Services, por 'name', por exemplo LoadBalance dos Pods
minikube service redirect-service --url | Mostra a URL externa do LoadBalance
mvn dockerfile:build | Compila um microserviço SpringBoot criando uma Imagem Docker