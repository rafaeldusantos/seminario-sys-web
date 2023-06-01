# seminario-sys-web
CRUD de livros em PHP, com Laravel e base de dados MySql externo\
\
Siga as instruções abaixo para acessar.\
\
Antes de tudo, você deve ter o Composer previamente instalados e uma servidor de banco de dados MYSQL ativo.\
\
Clone esse repositório em seu computador:
```sh
git clone https://github.com/rafaeldusantos/seminario-sys-web.git
```

Acesse o diretório da aplicação:
```sh
cd seminario-sys-web
```

Instale as dependências do projeto:
```sh
composer install
```

Crie um arquivo .env com a seguinte configuração (lembrando de alterar o DB_USERNAME e DB_PASSWORD conforme usuário e senha do seu MySQL):
```sh
APP_NAME="Seminário Aplicação WEB"
APP_ENV=local
APP_KEY=base64:iJXzkda9/rtjQM44VahiDo7Tape7peMkt4OOeAMYfwY=
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack
LOG_DEPRECATIONS_CHANNEL=null
LOG_LEVEL=debug

DB_CONNECTION=mysql
DB_HOST=localhost
DB_PORT=3306
DB_DATABASE=crud_books
DB_USERNAME=seu-usuario-banco
DB_PASSWORD=sua-senha-banco

BROADCAST_DRIVER=log
CACHE_DRIVER=file
FILESYSTEM_DRIVER=local
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

MEMCACHED_HOST=127.0.0.1

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379

MAIL_MAILER=smtp
MAIL_HOST=mailhog
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS=null
MAIL_FROM_NAME="${APP_NAME}"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_APP_CLUSTER=mt1

MIX_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
MIX_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"

```

Acesse seu servidor de banco de dados e crie a base de dados do projeto
```sh
create database crud_books;
```

O comando abaixo não é obrigatório, é somente para confirmar que a base foi criada corretamente. Se sim, vai aparecer crud_books na lista:
```sh
show databases;
```


Abra o terminal, navegue até a pasta do projeto e execute os seguinte comando para criar as tabelas na base de dados:
```sh
php artisan migrate
```

E use o seguinte comando para compilar e iniciar a aplicação.
```sh
php artisan serve --host=0.0.0.0
```
A aplicação está pronta para você acessar através da URL http://localhost:8000

