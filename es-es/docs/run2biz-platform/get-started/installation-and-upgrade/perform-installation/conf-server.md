Title: Configurando el servidor de aplicación

# Configurando el servidor de aplicación

Las configuraciones del servidor de aplicación se puede hacer de dos maneras: a través de jboss-cli o editando el archivo xml6. No hay diferencia técnica en ninguna de las opciones, y la elección depende de cada administrador. A continuación hay ambos ejemplos de configuración.

!!! Warning "ATENCIÓN"

    Esté atento a las variables para cambiarlas y adaptarlas según las configuraciones de entorno.

## Configurando servidor a través de jboss-cli

Conéctese a jboss-cli (suponiendo que el servidor se esté ejecutando) ejecutando el siguiente comando:

``` shell
[root@server /tmp]# /opt/wildfly/bin/jboss-cli.sh --connect
[standalone@localhost:9990 /]
```

Luego ejecute los siguientes comandos reemplazando los contenidos variables por la configuración de su entorno.

``` shell
[standalone@localhost:9990 /] /system-property=mongodb.host:add(value="citmongo")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=mongodb.port:add(value="27017")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=mongodb.user:add(value="admin")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=mongodb.password:add(value="admin")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.protocol:add(value="http")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.host:add(value="my.4biz.com")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.port:add(value="8080")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.context:add(value="4biz")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.login:add(value="4biz.local\\\consultor")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.password:add(value="senhaConsultor")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.inventory.id:add(value="4bizinventory")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.evm.id:add(value="4bizevm")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.evm.enable:add(value=true)
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.inventory.enable:add(value=true)
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.port.updateparameters:add(value="9000")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=4biz.inventory.pagelength:add(value="100")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=rhino.scripts.directory:add(value="")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=jboss.as.management.blocking.timeout:add(value="600")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=org.quartz.properties:add(value="$\{jboss.server.config.dir\}/quartz.properties")
{"outcome" => "success"}
[standalone@localhost:9990 /]/system-property=snmp.oid.repository.directory:add(value="/opt/templates")
{"outcome" => "success"}
```

Después de las configuraciones, para salir del CLI, escriba `quit`

``` shell
[standalone@localhost:9990 /] quit
[root@server /tmp]#
```
## Configurando el servidor a través de XML

Para editar el archivo XML utilizado por el wildfly a mano, ingrese en el directorio:

``` shell
[root@server /tmp]# /opt/wildfly/standalone/configuration
```
Y edite el archivo stantalone-full.xml e incluya la configuración XML 4biz justo después de la cláusula siguiente:

``` xml
<server xmlns="urn:jboss:domain:6.0">
    <extensions>
        <extension module="org.jboss.as.clustering.infinispan"/>
        <extension module="org.jboss.as.connector"/>
		...
</extensions>
```

 Después de cerrar la configuración `</extensions>` incluya el siguiente fragmento:

 ``` xml
 <system-properties>
     <property name="mongodb.host" value="citmongo"/>
     <property name="mongodb.port" value="27017"/>
     <property name="mongodb.user" value="admin"/>
     <property name="mongodb.password" value="admin"/>
     <property name="4biz.protocol" value="http"/>
     <property name="4biz.host" value="my.4bizcloud.com"/>
     <property name="4biz.port" value="8080"/>
     <property name="4biz.context" value="4biz"/>
     <property name="4biz.login" value="4biz.local\\\consultor"/>
     <property name="4biz.password" value="senhaConsultor"/>
     <property name="4biz.inventory.id" value="4bizinventory"/>
     <property name="4biz.evm.id" value="4bizevm"/>
     <property name="4biz.evm.enable" value="false"/>
     <property name="4biz.inventory.enable" value="false"/>
     <property name="rhino.scripts.directory" value=""/>
     <property name="jboss.as.management.blocking.timeout" value="600"/>
     <property name="4biz.port.updateparameters" value="9000"/>
     <property name="4biz.inventory.pagelength" value="100"/>
     <property name="org.quartz.properties" value="${jboss.server.config.dir}/quartz.properties"/>
     <property name="snmp.oid.repository.directory" value="/opt/templates"/>
 </system-properties>
 ```

 Después de configurar, reinicie el servicio para garantizar los cambios:

 ``` shell
 [root@server /tmp]# systemctl status wildfly
 ```

## Próximo paso

[Configurando el Datasource y Drives de base][1]

[1]:/es-es/4biz-helium/get-started/installation-and-upgrade/perform-installation/conf-datasource-and-db.html
