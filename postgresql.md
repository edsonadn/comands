# Comandos de instalación de Postgresql y Pgadmin

sudo apt update

sudo apt install postgresql postgresql-contrib

sudo su - postgres

## Entramos a la consola de postgresql

psql

create user curso with password 'Curso2021.';

create database db_curso with owner curso;

alter user curso with superuser;

# Instalamos pgadmin 4 

sudo apt install curl

curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add

sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'

sudo apt install pgadmin4

# inicio de base de datos

sudo -u postgres psql

\?    -> Ver los comandos postgres
\l    -> Listar todas las bases de datos
\dt   -> Ver las tablas de una base de datos
\h    -> Ver todos los comandos Sql
\g    -> Volver a ejecutar la funcion anterior

\c nombre_DB             -> Cambiar a otra base de datos
\d nombre_tabla          -> Describir una tabla
\h nombre_de_la_funcion  -> Ver como se ejecuta un comando sql
SELECT version();        -> Ver la version de postgres instalada
\timing 		 -> Inicializar el contador de tiempo


