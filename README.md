# My Teacher - Back-End

Esse repositório contém um projeto de backend escrito em Django, um framework para desenvolvimento de aplicações web em Python. Ele foi criado para o workshop "My Teacher", e é utilizado para gerenciar professores e aulas.

Para utilizar esse projeto, é necessário ter o Python instalado em sua máquina, além de instalar as dependências do projeto.

## Instalação das dependências

Para instalar as dependências do projeto, é recomendado criar um ambiente virtual (virtualenv). Isso permitirá que você instale as dependências do projeto sem afetar o Python globalmente em sua máquina. Para criar um ambiente virtual, execute o seguinte comando no terminal:

```python -m venv venv```

Esse comando criará uma pasta chamada "venv" no diretório atual, que conterá o ambiente virtual. Para ativá-lo, execute o seguinte comando:

```source venv/bin/activate```

Agora, o ambiente virtual está ativo e você pode instalar as dependências do projeto. Para isso, basta executar o seguinte comando:

```pip install -r requirements.txt```

Esse comando irá instalar todas as dependências listadas no arquivo "requirements.txt".

## Configurando o banco de dados
O projeto utiliza o banco de dados SQLite por padrão, mas você pode utilizar qualquer outro banco de dados compatível com o Django (como o PostgreSQL ou o MySQL). Para configurar o banco de dados, edite o arquivo "workshop_myteacher_backend/settings.py" e altere a configuração "DATABASES" de acordo com as suas necessidades.

Uma vez que o banco de dados esteja configurado, é preciso criar as tabelas necessárias para o projeto. Para isso, execute o seguinte comando:

```python manage.py makemigrations```

Esse comando irá criar os arquivos de migração, que são necessários para criar as tabelas no banco de dados. Em seguida, execute o seguinte comando para aplicar as migrações:

```python manage.py migrate```

## Criando um usuário administrador
Para acessar a área administrativa do Django e gerenciar professores e aulas, é necessário criar um usuário administrador. Para isso, execute o seguinte comando:

```python manage.py createsuperuser```

Esse comando irá solicitar que você informe o nome de usuário, e-mail e senha do novo usuário administrador. Depois de criado, você pode acessar a área administrativa pelo endereço http://localhost:8000/admin/.

## Gerenciando professores e aulas
Depois de criar o usuário administrador, você pode adicionar, editar e excluir professores e aulas na área administrativa do Django. Para isso, basta clicar no link "Professores" na barra de navegação à esquerda.

Gerando a API
O projeto também inclui uma API RESTful para permitir que o front-end acesse os dados dos professores e aulas. Para acessar a API, basta acessar o endpoints http://localhost:8000/professores/. Você pode utilizar essa API para exibir os professores e aulas no front-end do projeto.
