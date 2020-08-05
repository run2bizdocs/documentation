Title: Installation overview

# Instalation overview

Before starting the installation, it's necessary to understand all packages and components for the platform operation. Each component is responsible for a specific functionality to support the Platform, functionalities and ITIL Process.

* **4biz Enterprise Platform**: Package “WAR “(web application archive java) to be run under the wildfly application server. Mandatory in all scenarios.

* **Wildfly**: Java EE Web application server. Mandatory in all scenarios.

* **SOLR**: platform written in Java maintained by Apache used for indexing and searching text. It's necessary for indexing the texts of the 4biz Knowledge Base functionality.

* **MongoDB**: NoSQL database to store non-relational objects. Mandatory only for the use of inventory and event modules.

* **Active MQ**: Java message queue service developed and maintained by Apache. Mandatory in all scenarios.

* **Guacamole/GUACD**: Apache Guacamole is a remote desktop gateway without a client. Supports standard protocols like VNC, RDP and SSH. It is mandatory to establish remote access for support teams.

* **Tika**: Apache Tika is a toolkit that detects and extracts metadata and text from different types of file formats (such as PPT, XLS and PDF). Mandatory for the operation of the knowledge base.

* **Relational database**: The solution works with relational databases PostgreSQL, MSSQL Server and Oracle. In the next step, we will start installing all packages

!!! warning "ATTENTION"

     Some additional software and commands may be required depending on the operating system used. Some Linux distributions may not come by default with all sets of commands that will be executed next. In this case, we recommend installing the distribution packages used at any time.

	 
!!! tip "About"

    <b>Product/Version:</b> 4biz | Helium &nbsp;&nbsp;
    <b>Updated:</b>04/27/2020 - William Costa  
	
