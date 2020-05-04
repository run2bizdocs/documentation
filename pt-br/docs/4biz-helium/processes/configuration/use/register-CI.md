title: Cadastrar item de configuração
Description: Disponibiliza ações diversas, tais como, incluir, alterar e excluir um item de configuração. 

# Cadastrar item de configuração
Segundo a ITIL "Qualquer componente ou outro ativo de serviço que precise ser gerenciado de forma a entregar um serviço de TI".
Esta funcionalidade disponibiliza ações diversas, tais como, incluir, alterar e excluir um item de configuração.

Antes de começar
--------------------

Para registrar itens de configuração é necessário o cadastro prévio de um Acordo
de Nível de Serviço (Geral) do tipo "Disponibilidade", uma localidade, um
colaborador, um grupo, um contrato, um tipo de item de configuração e ao menos
um item de configuração principal, caso necessite criar outro item de
configuração relacionado.

Esta funcionalidade disponibiliza ações diversas, tais como, incluir, alterar e
excluir um item de configuração.

Procedimento
----------------

1.  Acessar a funcionalidade através da navegação no menu principal Processos \>
    Gerência de Configuração \> CMDB;

2.  Clicar no ultimo ícone da primeira linha da tela e em seguida clicar em
    "Criar novo dispositivo";

3.  Será apresentada a tela de cadastro com as abas de configuração do item de
    configuração;

4.  Preencher os campos disponíveis nas guias.

5.  Para a guia **Geral**, é necessário informar:

|Campo|Descrição|
|--------|---------|
|Identificação*|Uma ideficação para o IC que você está criando|
|Nome*|Nome do IC|
|Contrato|É possível registrar as informações de contratos e fornecedores do IC|
|Família|É possível informar a família do IC|
|Classe|Informe a classe do IC|
|Versão|É possível dizer qual é a versão do IC que você está criando|
|Número Série*|Identificar o número de série do IC|
|Unidade|É possível procurar a unidade que você deseja para o IC|
|Localidade*|O local do IC|
|Data Expiração|Data em que o IC expirará|
|Mídia|Você pode procurar a mídia que você criou|
|Tipo Item Configuração*|Você pode procurar o tipo de IC mais adequado|
|Status*|Aqui você tem uma série de opções para o IC, dependendo do status escolhido. Ao editar o IC, a ferramenta bloqueará a edição. Por exemplo, ao editar o IC e escolher o status "Destruído", a edição não será mais possível|
|Ativo Fixo|É possível informar os ativos fixos do IC|
|Criticidade do Serviço*|Aqui você pode definir o nível de criticidade para o serviço de IC|
|Intervalo de Período Crítico*|Configurar o período de criticidade do serviço|
|Impacto*|Você pode definir o grau de impacto|
|Urgência*|Você pode definir o grau de urgência|
|Colaborador|Você pode definir os funcionários para o IC usando uma caixa de pesquisa|
|Grupo*|Você pode selecionar o grupo que deseja para este IC|
|Mudança|Você pode procurar o número de uma mudança para o IC|
|Tipo de Responsável*|Você pode selecionar entre grupo e usuário|
|Responsável*|Você pode atribuir o IC através de uma caixa de pesquisa|
|Acordo de Nível de Serviço|Você pode pesquisar pelo título do SLA|
|Calendário|Você pode procurar pela descrição do calendário|
|TimeZone|Você pode pesquisar um fuso horário pelo nome|
|Custo por hora de indisponibilidade|Você pode definir o custo pelas horas em que o IC não está disponível|
|Item de configuração pai|Você pode informar um IC pai para este|
|Informações Adicionais|Aqui, você pode importar ou reportar automaticamente informações manuais, sobre o IC, por exemplo: ativos adquiridos de uma organização mesclada e ativos absorvidos em uma organização consolidada|
|Acesso Remoto|Aqui você pode definir a porta e a senha necessárias para o acesso remoto de um IC|

6. On the **Knowledge** tab, we have the option to Add a knowledge direct from the Knowledge Base.

When click on "Add Knowledge", it'll appear the screan to search for the knowledge you want to link to the CI you're creating and a list of documents already created.

To search for an specific knowledge, the filters available are: Title, Content, Published (Yes/No/All) and Situation.

!!! faq "Do you know..."
    
    On the creation of a Knowledge, it's possible to storage electronic and digital versions of physical
    documentation and asset documentation.
        
7. On the **Financial** tab, you'll have all information about apportionments (Service, Business Unit, Result Center, Account, Projects and Activities). Here you can edit it to add a new cost related.

    **Creating new Apportionment**
    
    1. Access the main menu Processes > Financial Management > Financial item;
    
    2. Complete the fields available on the **Information** tab:
    
    !!! note
    
        The system perform a hierarchical service-based costing model by the distribution of the cost model created in the financial process "Financial Item" and "Financial Cost Calculation" respecting the cost of each CI and making the distribution based on the cost model.
    
    |Field|Description|
    |---|---|
    |Type*|Cost/Expense, Budget, Revenue|
    | Classification* |(Capex, Opex, Fixed, Direct, Unit Cost, Indirect, Variable, Assessment)|
    |Forecast| it's available Only for Revenue and Costs/Expense Category (Used to simulate financial forecasts)|
    |Budget Account| Specific Account linked to this item|
    |Forecast financial item| It's possible to search for a title of the forecast financial item|
    |Due Date*|The date that will expire it|
    |Category*|The category for this|
    |Contract|Select a contract to be linked to it|
    |Cycle*|It's the financial Method, for example, Yarly, Monthly or Quarter|
    |Subcycle*|Depends on the Cycle|
    |Code|Freetext to create or insert financial code|
    |Title*|Title of this Financial Item|
    |Status*|It'll be always be created as "Pending"|
    |Description|Description about your financial item|
    
    3. On the **Values and Apportionments** tab, complete:
    
    |Field|Description|
    |---|---|
    |Entry type|There are two types: Value - if you set value, after the "Select services", it'll be presented a list with the service and its values; Accounting for activities performed - for this option, after Select the activities, it'll be presented the list with the activity you selected, as well as its information and description|
    |Expected value*| It's possible to stablish to number for the value expected|
    |Main value*| Set a number for the main value|
    |Additional*| Set the number for the additional|
    |Final value*| Set a number for the value end|
    |Apportionment| Here we have the options to set all the apportionments types|
    
    4. Click on save.
    
    

8. On the **Capacity** tab, it's possible to indicate the capacity/performance indicators that will be linked to this Configuration Items.

9. On the **Demand** tab, it's possible to search for a Demand to link in the Configuration Item.

On the **Warranties** tab, it'll be possible to set a time for the warranty of the Configuration Item.
By clicking on "Add warranty", it'll present a screen to configure it, they are:

|Field|Description|
|------|----------|
|Provider*|It's possible to search for a provider by its Name/Company Name or Individual Taxpayer's Registry/Corporate Taxpayer's ID|
|Start Date*|When the warranty starts to count|
|End Date*| When this warranty will have an end|

!!! faq "Do you know..."
    
    Once you are on the CMDB screen, on the right side of the screen, in the bottom, that's a box to identify the warranty of the CI you have registered on the Warranties tab

5.  Click on "Save" .

*Fields with ( * ) are mandatory*

### Comparing Versions of CI

1. Access the main menu Processes \>
    Configuration Management \> CMDB;
    
2. On the CMDB screen, select for a CI you want.

3. At the top of the screen, after the magnifier icon, click to see the options available.

4. Click on **Inventory status**. It'll appear the scream with all the options for status, for example: inventoried, ingnored, in execution and others. Select one of the status.

5. After select the status, by clicking on one of the items, it'll be possible to compare and verify the discrepancy between the previous versions of the item.  

### Verifying processes linked to the CI

Once created the CI, you can access it through the CI screen and link it to other preocesses of the tool.

|Item|Description|
|-----|----------|
|Reationship|It'll present the relationships with other processes|
|Request|It'll present all requests related to the configuration item|
|Incidents|It'll show all incidents related to the configuration item|
|Problems|It'll present all the problems related to the configuration item|
|Changes|It'll present all changes related to the configuration item, it is possible that the configuration item can only be changed with a linked change, to activate this rule go to Parameters> Number 85 and the tool will facilitate the prevention of changes in a configuration item without that has change|
|Releases|It'll present all releases related to the configuration item|
|Knowledges|It'll present all the knowledges related to the configuration item|
|Events|It'll show all events related to the configuration item|
|Financial|It'll present all finances related to the configuration item|
|Capacity|It'll present all the capabilities related to the configuration item|
|Demand|It'll present all the demands related to the configuration item|

We also have the information about:

|Item|Description|
|-----|----------|
|Warranties|It'll present all warranties of this configuration item|
|Impacted Services|	It'll present all impacted services of this configuration item|
|Remote access|	It'll present all remote access of this configuration item|
|Attachments|To attach documents to the CI|
|History|It'll present all history of this configuration item|

### Configuring capacity attributes

1. In the general settings of the configuration item, there is an option to enable the use of capacity indicators in that CI.

2. To configure capacity attributes, click on the **Capacity** item, located in the list of CI attributes (accessible on the left side of the screen).

3. Click on the icon for editing (the pencil icon) , in **notification** enable/disable the notifications for changes in capacity attributes. In the item **forecast**, indicate in percentage the level for sending notification relating to the capacity described

Relacionado
----------------

[Acordo de Nível de Serviço](/pt-br/4biz-helium/processes/service-level/use/service-level-agreement.html)

[Cadastrar um grupo](/pt-br/4biz-helium/initial-settings/access-settings/user/register-groups.html)

[Cadastrar um colaborador](/pt-br/4biz-helium/initial-settings/access-settings/user/register-employee.html)

[Cadastrar um contrato](/pt-br/4biz-helium/additional-features/contract-management/use/register-contract.html)

[Cadastrar localidade](/pt-br/4biz-helium/platform-administration/region-and-language/register-locations.html)

[Cadastrar tipo de item de configuração](/pt-br/4biz-helium/processes/configuration/configuration/register-type-ic.html)

!!! tip "About"

    <b>Product/Version:</b> 4biz | Helium &nbsp;&nbsp;
    <b>Updated:</b>01/15/2019 – Larissa Lourenço
