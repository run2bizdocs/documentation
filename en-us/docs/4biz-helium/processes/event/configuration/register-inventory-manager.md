title: Register Inventory manager
Description: Register and maintain the managers who will be responsible for the occurrences of events captured from 4biz Inventory.

Register Inventory manager
==========================

The purpose of this functionality is to register and maintain the managers who
will be responsible for the occurrences of events captured from 4biz Inventory.

It allows the user to indicate how much time the Manager will be processed, what
configuration items it will manage, the checks that will be applied and the
actions to be taken automatically.

This feature provides a variety of actions, such as including, changing, and
deleting Inventory manager.

Before getting started
----------------------

-   To register the Inventory manager, it's necessary to previously register the
    4biz Event Monitor connection, time, occurrence category, automatic action
    and the 4biz Inventory connection.

Procedure
---------

1.  Access the functionality through the main menu Processes \> Event Management
    \> Inventory Management \> Inventory Manager;

2.  Click on the desired Tab (Search / Register) and action;

| Function   | Description               |
|------------|---------------------------|
| **Add**    | Add Managers to the grids |
| **Save**   | Save the Managers         |
| **Delete** | Delete the Manager Edited |
| **Clear**  | Clear all Form Fields     |

Search
------

**Select the type of SLA to search for:**

| **Filter** | **Description**         |
|------------|-------------------------|
| Name       | Name to search          |
| Grid       | Grid with search result |

Register
--------

### BASIC DATA

1.  Complete the Basic Data:

| **Data Fields**      |
|----------------------|
| name (\*): Nome da conexão |
| Connection Inventory: Origem dos dados de monitoração oriundos de ferramentas internas e externas |

### SCHEDULER DATA

| **Data Fields**            |
|----------------------------|
| Enable/Disable AutoCorrect |
| Time for event closure     |

!!! NOTE

    A função de autocorreção é utilizada para arquivar eventos e fechar incidentes relacionados a eles, de maneira automática. A autocorreção depende da configuração do parâmetro "Time for event closure", que significa o intervalo de tempo para verificação de novos eventos.

### CONFIGURATION TYPE FOR CONFIGURATION ITEMS

| **Data Fields**                                                 |
|-----------------------------------------------------------------|
| Configuration Type(Specific Configuration,    General Settings) |

### CONFIGURATION ITEM PARENT

| **Data Fields**                          |
|------------------------------------------|
| Configuration item parent                |
| Category of occurrence group             |
| Category of occurrence                   |
| Generate occurrences of Up? (Yes / No )  |
| Action for up (Only register event)      |
| Urgency (Low/ Medium / High)             |
| Impact (Low/ Medium / High)              |
| Generate Down occurrences? ( Yes /  No ) |
| Action for down (Only register event)    |
| Urgency (Low/ Medium / High)             |
| Impact0                                  |

### CONFIGURATION ITEM CHILD  OR  TYPE OF CONFIGURATION ITEM

| **Data Fields**                                                               |
|-------------------------------------------------------------------------------|
| Configuration Type ( Configuration item child /   Type of Configuration Item) |
| Configuration item child                                                      |
| Check                                                                         |
| Category of occurrence group                                                  |
| Category of occurrence                                                        |
| Generate occurrences of Information? Yes No                                   |
| Condition for Information                                                     |
| Action for information                                                        |
| Urgency  (Low/ Medium / High)                                                 |
| Impact (Low/ Medium / High)                                                   |
| Generate Warning occurrences? ( Yes /  No )                                   |
| Condition for Warning                                                         |
| Action for warning                                                            |
| Urgency (Low/ Medium / High)                                                  |
| Impact (Low/ Medium / High)                                                   |
| Generate Exception occurrences?  ( Yes /  No )                                |
| Condition for Exception                                                       |
| Action for exception                                                          |
| Urgency (Low/ Medium / High)                                                  |
| Impact (Low/ Medium / High)                                                   |
| Configuration Type Configuration item child     Type of Configuration Item    |
| Configuration item child                                                      |
| Check                                                                         |
| Category of occurrence group                                                  |
| Category of occurrence                                                        |
| Generate occurrences of Information( Yes /  No )                              |
| Condition for Information                                                     |
| Value                                                                         |
| Action for information                                                        |
| Urgency (Low/ Medium / High)                                                  |
| Impact (Low/ Medium / High)                                                   |
| Generate Warning occurrences? ( Yes /  No )                                   |
| Condition for Warning                                                         |
| Value                                                                         |
| Action for warning                                                            |
| Urgency (Low/ Medium / High)                                                  |
| Impact (Low/ Medium / High)                                                   |
| Generate Exception occurrences?  ( Yes /  No )                                |
| Condition for Exception                                                       |
| Value                                                                         |
| Action for exception                                                          |
| Urgency (Low/ Medium / High)                                                  |
| Impact (Low/ Medium / High)                                                   |

(\*) Indicate mandatory field

!!! faq "Do you know?"

    For each block of information (Configuration Item Parent, Configuration Item Child or Type of Configuration Item), the follow configuration has the same meaning and values:   
    Action (Create incident, problem, change or send notification, Impact and Urgency to define the priority/criticity).

1.  Complete the fields available in each area;

2.  The completion fields will be changed as the *type of configuration* chosen:

    - **Specific Configuration:** it allows to create specific rules to a single
    configuration item. Those rules will be applied when the configuration item
    is being inventoried;

    - **General Settings:** it allows to create rules to all configuration items.
    Those rules will be applied when the configuration item is being
    inventoried.

3.  Ente the data necessary and click on "Add";

4.  Click on "Save".

Related
-------

[Register occurence category](/en-us/4biz-helium/processes/event/configuration/register-occurence-category.html)

[Register Event Monitor Connection](/en-us/4biz-helium/processes/event/configuration/register-event-monitor-connection.html)

[Register time](/en-us/4biz-helium/processes/event/configuration/register-time.html)

[Set Inventory connection](/en-us/4biz-helium/processes/event/configuration/set-inventory-connection.html)


!!! tip "About"

    <b>Product/Version:</b> 4biz | Helium &nbsp;&nbsp;
    <b>Updated:</b>01/04/2019 – Anna Martins
