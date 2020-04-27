Title: Installation overview

# Instalation overview

Before starting the installation, it's necessary to understand all the software necessary for the operation of the 16 certified processes of the platform. Each software plays a role within the solution, so it's necessary to understand the role of each one, the order of installation and the installation context itself. Depending on the type of installation (especially which processes will be implemented) it's not necessary to install all of them. Below the software that comprises the 4biz Workflow platform:

* **4biz Enterprise Platform**: Platform package in java WAR (web application ARchive) to be installed in the wildfly. Mandatory in all scenarios.

* **Wildfly**: Java EE Web application server. Mandatory in all scenarios.

* **SOLR**: platform written in Java maintained by Apache used for indexing and searching text. It's necessary for indexing the texts of the 4biz Workflow knowledge module. Mandatory for the operation of the knowledge base.

* **MongoDB**: NoSQL database to store non-relational objects. Mandatory only for the use of inventory and event modules.

* **Active MQ**: Java message queue service developed and maintained by Apache. Mandatory in all scenarios.

* **Guacamole/GUACD**: Apache Guacamole is a remote desktop gateway without a client. Supports standard protocols like VNC, RDP and SSH. It is mandatory to establish remote access for support teams.

* **Tika**: Apache Tika is a toolkit that detects and extracts metadata and text from different types of file formats (such as PPT, XLS and PDF). Mandatory for the operation of the knowledge base.

* **Relational database**: The solution works with relational databases PostgreSQL, MSSQL Server and Oracle. If you have the option to choose any of them, we suggest that you give preference to PostgreSQL, as it is the most used in most installations. MSSQL Server and Oracle banks are supported with some adjustments. Consult our technical support for details of the version supported by these last two banks

In the next step, we will start installing all packages

!!! warning "ATTENTION"

     Some additional software and commands may be required depending on the operating system used. Some Linux distributions may not come by default with all sets of commands that will be executed next. In this case, we recommend installing the distribution packages used at any time.

	 
!!! tip "About"

    <b>Product/Version:</b> 4biz | Helium &nbsp;&nbsp;
    <b>Updated:</b>04/27/2020 - William Costa  
	
