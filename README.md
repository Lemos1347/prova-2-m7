# Exemplo funcionando

https://github.com/Lemos1347/prova-2-m7/assets/99190347/bbbefa23-b2ac-4997-aba5-76bdcdc45f71

# Tarefas efetuadas

## Banco de dados
- Criação de um banco de dados, um RDS na AWS.
- Após isso, foi alterada as credenciais de conexão ao banco de dados dos arquivos da [backend](/backend).
- Por fim, foi executado o script python para a criação das tabelas no banco de dados.

## Backend
- Criei uma instância EC2 na AWS.
- Instalei o Docker na EC2.
- Alterei o "security group" para permitir conexões na porta 8000.
- Criei um Dockerfile apropriado para a aplicação: (Dockerfile)[/backend/Dockerfile].
- Subi essa imagem para o Docker Hub: (link)[https://hub.docker.com/repository/docker/lemos12/backend-prova-2-m7/general]
- Baixei essa imagem na EC2.
- Rodei um container com um bind de portas de 8000 para 8000.

## Frontend
- Criei uma instância EC2 na AWS.
- Instalei o Docker na EC2.
- Alterei o "security group" para permitir conexões na porta 3002.
- Alterei o ip para o qual o frontend estava fazendo a conexão (apontei para o ip e porta correta do backend).
- Criei um Dockerfile com a imagem "Apache" padrão e copiei os arquivos adequados para a pasta adequada do apache: (Dockerfile)[/frontend/Dockerfile]
- Subi essa imagem para o Docker Hub: (link)[https://hub.docker.com/repository/docker/lemos12/frontend-prova-2-m7-10/general]
- Baixei essa imagem no EC2.
- Rodei um container com um bind de portas de 3002 para 80.

# Template para avaliação P2

Saída esperada após execução do programa:

<img src="./media/tela-front.png" display="flex">

# IMPORTANTE:

Para colocar o frontend para funcionar, colocar uma máquina EC2 rodando o Apache WebServer.
Para isso, instalar dentro da EC2:

```bash
sudo apt update
sudo apt upgrade
sudo apt install apache2
# os arquivos do projeto devem estar em /var/www/html
git clone https://github.com/Murilo-ZC/Avaliacao-P2-M7-2023-EC.git
sudo cp ./Avaliacao-P2-M7-2023-EC/frontend /var/www/html
```

Aqui pessoal, os arquivos já estaram disponíveis na porta 80, não necessário redirecionar.

> IMPORTANTE: Verificar as rotas e utilziar o seu próprio repositório com as modificações realizadas.
