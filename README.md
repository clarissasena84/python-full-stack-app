# python-full-stack-app
# To‑Do App com Flask + MySQL

## Descrição
Aplicação de lista de tarefas (To‑Do) com categorias. Back-end em Flask, front-end em HTML/CSS/JS e dados persistentes em MySQL.

## Requisitos
- Python 3
- Flask
- MySQL
- Navegador web

## Instalar dependências
 pip install flask flask-cors mysql-connector-python

## Criar base de dados
sudo mysql

CREATE DATABASE todo_app;
USE todo_app;

CREATE TABLE todos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    text VARCHAR(255) NOT NULL,
    done BOOLEAN DEFAULT FALSE,
    category_id INT,
    FOREIGN KEY (category_id) REFERENCES categories(id)
);

CREATE TABLE categories (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50) NOT NULL
);

## Iniciando o projeto
### Certificando-se que o flask e o mysql-connector-python estão instalados
sudo apt update
sudo apt install -y mysql-server python3-flask python3-pip

### Utilizando o venv para melhor gestão de recursos
##### 1. Garante que o módulo de venv está instalado
sudo apt update
sudo apt install python3-venv -y

##### 2. Cria o ambiente virtual
python3 -m venv venv

##### 3. Ativa o ambiente virtual
source venv/bin/activate

##### 4. Instala as dependências dentro do venv
pip install flask mysql-connector-python


## Montando estrutura dos arquivos
- Criar uma pastinha templates  e lá dentro criar o index.html 
- Criar uma pastinha static  e lá dentro criar o style.css e o app.js 
- Os arquivos app.py e requirements.txt devem estar na raiz do projeto

## Rota do Randon (ao acessar executa a função rodando de números aleatórios)
http://localhost:5000/ali/todos/random
