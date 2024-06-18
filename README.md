# projet-infra
Aplicação Web Simples com Contêineres Docker e Ansible para a disciplina de Infraestrutura e Serviços Web.

##Estrutura do projeto:
projeto-infra/
├── frontend/
│   ├── Dockerfile
│   └── src/      //foi aproveitado o trabalho de IHM para exemplo deste projeto
│       └── index.html
|       └── css
|       └── img
|       └── javascript
|       └── importancia.html
|       └── obrigado.html
|       └── diferencial.html
|       └── servico.html
|       └── contato.html
├── backend/
│   ├── Dockerfile
│   ├── requirements.txt
│   └── app/
│       └── main.py
├── database/
│   └── Dockerfile
└── ansible/
    └── playbook.yml

##Requisitos:
-Docker
-Ansible

##Comandos essenciais para executar o projeto:
1. Criando a rede "net"
sudo docker network create net

2. Rodando o contêiner Frontend:
sudo docker build -t myfrontend ./frontend
sudo docker run -d --name frontend --network net -p 80:80 myfrontend

3. Rodando o contêiner Backend:
sudo docker build -t mybackend ./backend
sudo docker run -d --name backend --network net mybackend

4. Rodando o contêiner Database:
sudo docker build -t mydatabase ./database
sudo docker run -d --name database --network net mydatabase

5. Rodando o Ansible:
sudo ansible-playbook playbook.yml //no diretório "ansible"
sudo ansible-playbook ansible/playbook.yml //no diretório "projeto-infra"

6. Acessando a página Web:
http://localhost


