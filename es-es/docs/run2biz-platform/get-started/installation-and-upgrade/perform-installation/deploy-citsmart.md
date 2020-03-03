Title: Haciendo deploy de 4biz

# Haciendo deploy de 4biz

Descargue el paquete 4biz y Builder WAR del portal de socios. Enviar al servidor usando scp a la carpeta /tmp. La instalación de 4biz consta de los siguientes pasos:

1. Implemente el paquete de 4biz tracker
2. Implemente el paquete Builder
3. Realizar la configuración inicial del 4biz tracker

Descomprima el paquete del 4biz tracker si está en formato .zip:

``` shell
[root@server /tmp]# unzip 4bizITSM-Enterprise-8.0.2.0.war.zip
```

Copie al servidor de aplicaciones en la carpeta `standalone/deployments`:

``` shell
[root@server /tmp]# cp 4bizITSM-Enterprise-8.0.2.0.war /opt/wildfly/standalone/deployments/
```
Observe el log `/opt/wildfly/standalone/log/server.log` con la opción `tail -f` hasta que aparezca el siguiente mensaje:

``` shell
2019-11-14 17:20:37,731 INFO  [org.jboss.as.server] (DeploymentScanner-threads - 1) WFLYSRV0010: Deployed "4bizITSM-Enterprise-8.0.2.0.war" (runtime-name : "4bizITSM-Enterprise-8.0.2.0.war")
```

El mensaje anterior confirma que se realizó la implementación. Lo mismo se aplica al paquete Builder. Copie el Builder a la carpeta `standalone/deployments`:

``` shell
[root@server /tmp]# cp 4biz-Builder-web-1.3.2.1.war /opt/wildfly/standalone/deployments/
```

Observe el log `/opt/wildfly/standalone/log/server.log` con la opción `tail -f` hasta que aparezca el siguiente mensaje:

``` shell
2019-11-14 17:37:43,647 INFO  [org.jboss.as.server] (DeploymentScanner-threads - 2) WFLYSRV0010: Deployed "4biz-Builder-web-1.3.2.1.war" (runtime-name : "4biz-Builder-web-1.3.2.1.war")
```

## Accediendo a 4biz por la primera vez

Después de la implementación, acceda a 4biz a través de la URL: si se ha configurado un dominio, vaya a la ruta https://DOMINIO/4biz, si lo configura a través de IP, vaya a https://ENDERECO_IP/4biz.

!!! info "Navegadores Soportados"
    Para un funcionamiento adecuado del sistema, debe usar las siguientes versiones mínimas de los principales navegadores: **Microsoft EDGE** (Edge 42.17134.0 / Microsoft EdgeHTML 17.17134 o superior); **Google Chrome** (versión 76.0.3809.132 o superior); **Mozila Firefox** (versión 69.0 o superior).

## Próximo paso

[Finalizar instalación][1]

[1]:/es-es/4biz-helium/get-started/installation-and-upgrade/perform-installation/setup-4biz.html
