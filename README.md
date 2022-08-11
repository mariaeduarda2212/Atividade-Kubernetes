# Programa de bolsas DevSecOps CompassUol- Grupo 4- Trilha de Kuberbetes

Componentes do grupo: Flavio Henrique Almeida Junior, Maria Eduarda Araújo de Oliveira, Moises Francisco Ximenes De Souza e Ryan Do Rosario Santos Amaro.


## Projeto

O projeto em questão foi solicitado pela empresa Compass UOL especificamente como atividade prática no desenvolvimento da trilha kubernetes. Referente ao estágio de DevSecOps.

Os instrutores solicitaram na atividade que criassemos um namespace chamado labwordpress e tudo que fizermos deverá estar dentro desse namespace.

Desta forma, no final da atividade devemos verificar se os pods, os services e os pvcs foram criados corretamente dentro do namespace criado no início da atividade;

Ainda, é necessário verificar qual foi a URL gerada através do ingress do Kubernetes e copiar essa URL do Ingress e colar no browser para abrir a tela inicial do wordpress;


## Desenvolvimento
Para esse desenvolvimento, iremos utilizar o docker for windows

## Tarefas
Para essa atividade foram solicitadas as seguintes tarefas:

[T-01] Crie um namespace chamado labwordpress, tudo o que for feito deverá estar dentro deste namespace;

[T-02] Faça o apply do arquivo de service do MySQL mude a porta padrão do banco MySQL para 3308;

[T-03] Crie o arquivo secret que deverá conter o password do banco MySQL, lembre-se de criar uma senha com fortes padrões de segurança;

[T-04] Faça o apply do arquivo de PersistentVolumeClaim do MySQL para um capacity de 3GB;

[T-05] Faça o apply do arquivo de deployment do MySQL, crie também um volume mount no deployment do MySQL chamado “mysql-persistent-storagelab", apontando para /var/lib/mysql. Lembre-se de criar o volume em si com o mesmo nome do volume mount;

[T-06] Faça o apply do arquivo de service do Wordpress altere para a TCP Port 80;

[T-07] Faça o apply do arquivo de PersistentVolumeClaim do Wordpress, para um capacity de 3GB;

[T-08] No arquivo de deployment do Wordpress, crie um volume mount no deployment do Wordpress chamado “wordpresspersistent-storage-lab", apontando para /var/www/html. Lembre-se de criar o volume em si com o mesmo nome do volume mount;

[T-09] No arquivo de deployment do wordpress, insira o secret contendo o password do MySQL, criado no começo do exercício.

[T-10] Faça o apply do arquivo de deployment do wordpress;

[T-11] Verifque se os pods, os services e os pvcs foram criados da forma correta dentro namespace criado no início deste exercício;

[T-12] Verifique qual foi a URI gerada através do ingress do Kubernetes;

[T-13] Copie essa URI do Ingress e cole no browser para abrir a tela inicial do wordpress

[T-14] Criar documentação


## Pods, services e pvcs criados  

kubectl get pods --namespace=labwordpress

kubectl get services --namespace=labwordpress

kubectl get pvcs --namespace=labwordpress

## URL do Ingress

kubectl describe pod wordpress -n labwordpress

## Entrega
Deverá ser desenvolvida a atividade em questão e entregue através do Github e com a documentação do READ.ME.

Segue-se um link mais detalhado dos comandos usados desse projeto:

Documentação da Atividade: https://scented-drain-3ab.notion.site/Atividade-Kubernetes-6ba728ba159a491d87f51dc8f7ac8e1b

A documentação deverá ser concluida e entregue até 11/08/2022 às 10:00.
A apresentação será o dia 12/08/2022 às 14:30. 
