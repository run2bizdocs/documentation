Title: Configurando el Datasource y Drives de base

# Configurando el Datasource y Drives de base

Antes de crear un datasource, se debe agregar un módulo de base de datos al sistema. Cada base tiene su propio driver de conexión, pero todas las configuraciones asumen el mismo principio: descargar el driver del fabricante, cópielo en wildfly, configúrelo en el sistema. La configuración se realizará a través de jboss-cli, pero todos se pueden realizar a través de XML en el archivo standalone-full.xml si lo desea.

En el siguiente ejemplo usaremos el driver PostgreSQL. Cada base de datos tiene su propio método de configuración, recomendamos buscar en la documentación del fabricante de la base de datos de su elección si difiere de nuestra documentación.

La descarga del driver JDBC de PostgreSQL se puede encontrar en https://jdbc.postgresql.org en el enlace de descargas. La versión del driver utilizada por 4biz es 4.1 build 9.3 Build 1104.

```sh
[root@server /tmp]# wget https://jdbc.postgresql.org/download/postgresql-9.3-1104.jdbc41.jar
```

Acceda nuevamente a jboss-cli para agregar el driver con el siguiente comando (suponiendo que lo haya descargado en la carpeta `/tmp`):

```sh
[standalone@localhost:9990 /] module add --name=org.postgres --resources=/tmp/postgresql-9.3-1104.jdbc41.jar --dependencies=javax.api,javax.transaction.api
```

Con este comando, el driver se agregará automáticamente a la carpeta `/opt/wildfly-12.0.0.Final/modules/org/postgres/main/`

Continúe con la CLI y ejecute el siguiente comando para agregar un datasource:

```sh
[standalone@localhost:9990 /] /subsystem=datasources/jdbc-driver=postgres:add(driver-name="postgres",driver-module-name="org.postgres",driver-xa-datasource-class-name=org.postgresql.xa.PGXADataSource
```

## Creando la base de datos de 4biz

Independientemente de la arquitectura de la base (ya sea instalada en el mismo servidor o separado), los pasos a continuación son para crear una base de datos y un usuario para 4biz. En el procedimiento asumimos que tiene acceso al SGBD. Acceda al PostgreSQL con el comando a continuación:

```sh
[root@server /tmp]#  su - postgres
bash-4.2$
bash-4.2$ psql
psql (9.6.15)
Type "help" for help.

postgres=#
```
Cree un nombre de usuario y contraseña de acceso a la base de 4biz (reemplace la SU_CONTRASEÑA con una contraseña preferida):

```sh
postgres=# create user 4bizdbuser with password 'SUA_SENHA';
CREATE ROLE
postgres=#
```
Crear una base de datos para 4biz:

```sh
postgres=# create database 4biz_db with owner 4bizdbuser encoding 'UTF8' tablespace pg_default;
CREATE DATABASE
postgres=#
```
Dar permiso al usuario de 4biz:

```sh
postgres=# alter role 4bizdbuser superuser;
ALTER ROLE
postgres=#
```

Salga del PSQL y del shell del usuario de postgres:

```sh
postgres=# \q
bash-4.2$ exit
exit
[root@server /tmp]#
```
Si la base se está ejecutando en el mismo servidor, es necesario liberar la conexión al usuario de 4biz. Edite el archivo  `/var/lib/pgsql/9.6/data/pg_hba.conf` e incluye la siguiente línea:

```sh
# Database administrative login by Unix domain socket
local   all             postgres                                ident
```
!!! Warning "ATENCIÓN"

    No cambie la línea `local all postgres peer` que viene por defecto, incluya la línea de arriba justo debajo de esta.


Si la base de datos se ejecuta en otro servidor, es necesario liberar la conexión desde Wildfly. Para hacer esto, incluya la siguiente línea en el mismo archivo pg_hba.conf, reemplazándolo con la dirección IP del servidor Wildfly:

```sh
host 4biz_db 4bizdbuser WILDFLY_IP_ADDRESS/32 md5

```

## Configurando el datasource para 4biz

Hay ocho entradas de datasource para 4biz_db, cuatro para 4biz y cuatro para 4biz Builder. El nombre de usuario y la contraseña son 4bizdbuser y SU_CONTRASEÑA, creados en el paso anterior. Si creó un nombre de usuario, contraseña y base de nombres diferentes, cámbielo en los comandos abajo.

Conéctese a jboss-cli y ejecute los siguientes comandos:

### Datasource 4biz

```sh
/subsystem=datasources/data-source="/jdbc/4biz":add(jndi-name="java:/jdbc/4biz",driver-name="postgres",connection-url="jdbc:postgresql://pgdata.4biz.com:5432/4biz_db",user-name="4bizdbuser",password="exemplo123",driver-class="org.postgresql.Driver", enabled=true, use-java-context=true)
/subsystem=datasources/data-source="/jdbc/4biz":write-attribute(name=min-pool-size,value=10)
/subsystem=datasources/data-source="/jdbc/4biz":write-attribute(name=max-pool-size,value=300)
/subsystem=datasources/data-source="/jdbc/4biz":write-attribute(name=pool-prefill,value=true)
/subsystem=datasources/data-source="/jdbc/4biz":write-attribute(name=flush-strategy,value=FailingConnectionOnly)
/subsystem=datasources/data-source="/jdbc/4biz":write-attribute(name=blocking-timeout-wait-millis,value=60000)
/subsystem=datasources/data-source="/jdbc/4biz":write-attribute(name=idle-timeout-minutes,value=5)
```

### Datasource 4bizFlow

```sh
/subsystem=datasources/data-source="/jdbc/4bizFluxo":add(jndi-name="java:/jdbc/4bizFluxo",driver-name="postgres",connection-url="jdbc:postgresql://pgdata.4biz.com:5432/4biz_db",user-name="4bizdbuser",password="exemplo123",driver-class="org.postgresql.Driver", enabled=true, use-java-context=true)
/subsystem=datasources/data-source="/jdbc/4bizFluxo":write-attribute(name=min-pool-size,value=10)
/subsystem=datasources/data-source="/jdbc/4bizFluxo":write-attribute(name=max-pool-size,value=300)
/subsystem=datasources/data-source="/jdbc/4bizFluxo":write-attribute(name=pool-prefill,value=true)
/subsystem=datasources/data-source="/jdbc/4bizFluxo":write-attribute(name=flush-strategy,value=FailingConnectionOnly)
/subsystem=datasources/data-source="/jdbc/4bizFluxo":write-attribute(name=blocking-timeout-wait-millis,value=60000)
/subsystem=datasources/data-source="/jdbc/4bizFluxo":write-attribute(name=idle-timeout-minutes,value=5)
```

### Datasourece 4biz_reports

```sh
/subsystem=datasources/data-source="/jdbc/4biz_reports":add(jndi-name="java:/jdbc/4biz_reports",driver-name="postgres",connection-url="jdbc:postgresql://pgdata.4biz.com:5432/4biz_db",user-name="4bizdbuser",password="exemplo123",driver-class="org.postgresql.Driver", enabled=true, use-java-context=true)
/subsystem=datasources/data-source="/jdbc/4biz_reports":write-attribute(name=min-pool-size,value=10)
/subsystem=datasources/data-source="/jdbc/4biz_reports":write-attribute(name=max-pool-size,value=300)
/subsystem=datasources/data-source="/jdbc/4biz_reports":write-attribute(name=pool-prefill,value=true)
/subsystem=datasources/data-source="/jdbc/4biz_reports":write-attribute(name=flush-strategy,value=FailingConnectionOnly)
/subsystem=datasources/data-source="/jdbc/4biz_reports":write-attribute(name=blocking-timeout-wait-millis,value=60000)
/subsystem=datasources/data-source="/jdbc/4biz_reports":write-attribute(name=idle-timeout-minutes,value=5)
```

### Datasource 4bizBpmEventos

```sh
/subsystem=datasources/data-source="/jdbc/4bizBpmEventos":add(jndi-name="java:/jdbc/4bizBpmEventos",driver-name="postgres",connection-url="jdbc:postgresql://pgdata.4biz.com:5432/4biz_db",user-name="4bizdbuser",password="exemplo123",driver-class="org.postgresql.Driver", enabled=true, use-java-context=true)
/subsystem=datasources/data-source="/jdbc/4bizBpmEventos":write-attribute(name=min-pool-size,value=10)
/subsystem=datasources/data-source="/jdbc/4bizBpmEventos":write-attribute(name=max-pool-size,value=300)
/subsystem=datasources/data-source="/jdbc/4bizBpmEventos":write-attribute(name=pool-prefill,value=true)
/subsystem=datasources/data-source="/jdbc/4bizBpmEventos":write-attribute(name=flush-strategy,value=FailingConnectionOnly)
/subsystem=datasources/data-source="/jdbc/4bizBpmEventos":write-attribute(name=blocking-timeout-wait-millis,value=60000)
/subsystem=datasources/data-source="/jdbc/4bizBpmEventos":write-attribute(name=idle-timeout-minutes,value=5
```

### Datasource 4biz-Builder

```sh
/subsystem=datasources/data-source="/env/jdbc/4biz-Builder":add(jndi-name="java:/env/jdbc/4biz-Builder",driver-name="postgres",connection-url="jdbc:postgresql://pgdata.4biz.com:5432/4biz_db",user-name="4bizdbuser",password="exemplo123",driver-class="org.postgresql.Driver", enabled=true, use-java-context=true)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=min-pool-size,value=10)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=max-pool-size,value=300)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=pool-prefill,value=true)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=flush-strategy,value=FailingConnectionOnly)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=blocking-timeout-wait-millis,value=60000)#
```

### Datasource 4biz-Builder-app1

```sh
/subsystem=datasources/data-source="/env/jdbc/4biz-Builder-app1":add(jndi-name="java:/env/jdbc/4biz-Builder-app1",driver-name="postgres",connection-url="jdbc:postgresql://pgdata.4biz.com:5432/4biz_db",user-name="4bizdbuser",password="exemplo123",driver-class="org.postgresql.Driver", enabled=true, use-java-context=true)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=min-pool-size,value=10)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=max-pool-size,value=300)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=pool-prefill,value=true)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=flush-strategy,value=FailingConnectionOnly)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=blocking-timeout-wait-millis,value=60000)
```

### Datasource 4biz-Builder-app2

```sh
/subsystem=datasources/data-source="/env/jdbc/4biz-Builder-app2":add(jndi-name="java:/env/jdbc/4biz-Builder-app2",driver-name="postgres",connection-url="jdbc:postgresql://pgdata.4biz.com:5432/4biz_db",user-name="4bizdbuser",password="exemplo123",driver-class="org.postgresql.Driver", enabled=true, use-java-context=true)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=min-pool-size,value=10)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=max-pool-size,value=300)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=pool-prefill,value=true)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=flush-strategy,value=FailingConnectionOnly)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=blocking-timeout-wait-millis,value=60000)
```
### Datasource 4biz-Builder-app3

```sh
/subsystem=datasources/data-source="/env/jdbc/4biz-Builder-app3":add(jndi-name="java:/env/jdbc/4biz-Builder-app3",driver-name="postgres",connection-url="jdbc:postgresql://pgdata.4biz.com:5432/4biz_db",user-name="4bizdbuser",password="exemplo123",driver-class="org.postgresql.Driver", enabled=true, use-java-context=true)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=min-pool-size,value=10)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=max-pool-size,value=300)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=pool-prefill,value=true)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=flush-strategy,value=FailingConnectionOnly)
/subsystem=datasources/data-source="/env\/jdbc\/4biz-Builder":write-attribute(name=blocking-timeout-wait-millis,value=60000)
```

Antes de salir de jboss-cli, ejecute el comando reload para aplicar los cambios y realizar una prueba de conexión de la base de datos:

```sh
[standalone@localhost:9990 /]: reload
```
Y haga una prueba de conexión con todos las bases con los siguientes comandos. Recordando que el resultado debe ser `"outcome" => "success"`:

``` sh
/subsystem=datasources/data-source="/jdbc/4biz":test-connection-in-pool
/subsystem=datasources/data-source="/jdbc/4bizFluxo":test-connection-in-pool
/subsystem=datasources/data-source="/jdbc/4biz_reports":test-connection-in-pool
/subsystem=datasources/data-source="/jdbc/4bizBpmEventos":test-connection-in-pool
/subsystem=datasources/data-source="/jdbc/4biz-Builder":test-connection-in-pool
/subsystem=datasources/data-source="/jdbc/4biz-Builder-app1":test-connection-in-pool
/subsystem=datasources/data-source="/jdbc/4biz-Builder-app2":test-connection-in-pool
/subsystem=datasources/data-source="/jdbc/4biz-Builder-app3":test-connection-in-pool
```

## Próximo paso

[Configurando el Wildfly][1]

[1]:/es-es/4biz-helium/get-started/installation-and-upgrade/perform-installation/conf-wildfly.html
