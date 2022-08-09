#Programa de bolsas DevSecOps CompassUol- Atividade 11- Trilha Linux e atividade de redes.

#Componentes do grupo: Flavio Henrique Almeida Junior, Maria Eduarda Araújo de Oliveira, Moises Francisco Ximenes De Souza e Ryan Do Rosario Santos Amaro.

##Projeto

O projeto em questão foi solicitado pela empresa Compass UOL especificamente como atividade prática no desenvolvimento da trilha kubernetes. Referente ao estágio de DevSecOps.

Os instrutores solicitaram na atividade que subíssemos um segundo servidor Oracle Linux seguindo as configurações da Maquina Virtual da atividade anterior, sem interface gráfica, adicionando algumas alterações no desenvolvimento do projeto.

Desta forma, devemos mudar a VLAN das duas de Nat para Modo Bridge realizando os ajustes necessários, realizando a relação de consiança entre as duas Máquinas Vituais.

Ainda, é necessário criar um slide respondendo as perguntas especificas feitas pelos instrutores e uma documentação explicando qual o processo para instalação do linux, bem como realizar o versionamento da atividade.

##Desenvolvimento
Para esse desenvolvimento, iremos usar virtualbox como um ambiente virtual usaremos a ISO do ORACLE LINUX.

##Tarefas
Para essa aplicação serão necessárias as seguintes tarefas:

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


##Configuração de redes

#Maquina Server:
[IP] 10.0.2.17(classe A);

[Netmask] 255.255.255.0(/24);

[Gateway] 10.0.2.2;

[DNS] server;

[HOSTNAME] compass.atividade11server;

#Maquina Client
[IP] 10.0.2.17(classe A);

[Netmask] 255.255.255.0(/24);

[Gateway] 10.0.2.2;

[DNS] client;

[HOSTNAME] compass.atividade11client;

##Entrega
Deverá ser desenvolvido a aplicação em questão e entregue através do Github e com a documentação do READ.ME.

Segue-se um link mais detalhado dos comandos usados desse projeto:

[Comandos Utilizados na Atividade.docx](https://github.com/mariaeduarda2212/atividade11/files/9162607/Comandos.Utilizados.na.Atividade.docx)

[Apresentação da Atividade11.pptx](https://github.com/mariaeduarda2212/atividade11/files/9169169/Apresentacao.da.Atividade11.pptx)

[Documentação Linux.pdf](https://github.com/mariaeduarda2212/atividade11/files/9168843/Documentacao.Linux.pdf)

Documentação da Atividade: https://scented-drain-3ab.notion.site/Atividade-Kubernetes-6ba728ba159a491d87f51dc8f7ac8e1b

A documentação deverá ser concluida e entregue até 11/08/2022 às 10:00.
A apresentação será o dia 12/08/2022 às 14:30.
