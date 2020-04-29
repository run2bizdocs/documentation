title: Cadastrar uma mudança
Description: Tem por objetivo registrar uma mudança. 
# Cadastrar uma mudança 

Esta funcionalidade tem por objetivo registrar uma mudança. Segundo a ITIL, é necessário formalizar a solicitação de mudança, para que seja registrado pela equipe responsável todos os procedimentos realizados para a alteração desejada (desde a sua requisição ao impacto de sua implementação) monitorando o mesmo por todo o seu ciclo de vida.

Antes de começar
------------------

 Para efetivar o cadastro de uma mudança é preciso previamente cadastrar um contrato, uma unidade e que ela esteja vinculada ao contrato, um colaborador, um questionário, o Comitê Consultivo de Mudanças, ter um grupo vinculado ao contrato associado os Solicitantes (colaboradores) já cadastrados a este grupo. Caso seja preciso criar um novo colaborador, é necessário incluí-lo ao Grupo de Solicitante no qual esteja relacionado ao contrato.
Ademais, é fundamental o cadastro prévio do portfólio de mudanças.

Procedimento 
--------------

1.	Acessar a funcionalidade através da navegação no menu principal Processos > Gerência de Mudança > Mudança;
2.	Clicar no botão “Opções” e em seguida em “Cadastro”;
3.	Preencher todos os campos disponíveis:

### Solicitante

Para identificar o solicitante da mudança, complete os campos:

|Campos|Descrição|
|---|---|
|Nome (\*)|Nome completo do solicitante|
|Contato (\*)|Identificar o contato do usuário|
|E-mail (\*)|E-mail do usuário|
|Telefone|Número de telefone do usuário|
|Ramal|O número do ramal do usuário|
|Unidade (\*)|Unidade do usuário|
|Localidade Física|A localização física do usuário|
|Outras Informações|Informação adicional sobre o usuário|

(*) Indicar campos obrigatórios

### Mudança

Para identificar a mudança, preencha os campos:

|Campos|Descrição|
|---|---|
|Título (\*)|Título para identificar a mudança|
|Descrição da alteração (\*)|Descrição da mudança|
|Efeito de não implementar a mudança|Efeito caso a mudança não for implementada|
|Contrato|Contrato vinculado a mudança|
|Importância|O nível de importância da mudança. Apresenta as seguintes opções: **Importante** envolve uma quantidade significativa de preparação e trabalho com situações complexas ou grandes;**Significante** mudança significativa, mudanças significativas envolvem preparação e trabalho, avaliação, autorização e planejamento de mudanças. Exemplos: Compra e instalação de um novo servidor, Re-segmentação de rede;**Pequena** pode ser avaliado e autorizado fora da autoridade do CCM (por exemplo, por um coordenador).|
|Impacto|Impacto que a mudança gera, temos as opções: **Baixa**, **Média** e **Alta**.|
|Urgência|Urgência para realizar a mudança, temos as opções: **Baixa**, **Média** e **Alta**|
|Grupo Executor|O grupo responsável pela execução da mudança|
|Notificações|Definir as notificações entre "Enviar email ao criar a Mudança", "Enviar email ao finalizar a Mudança", "Enviar email para o comitê consultivo de mudança", "Enviar email para as demais ações da Mudança"|

(*) Indicar campos obrigatórios

!!! Abstract "NOTA"
    
        Para [Criar portfólio de mudança](/pt-br/4biz-helium/processes/change/configuration/change-portfolio.html)
        
### Anáise ágil de risco

Na área de análise de riscos, serão feitas três questões:

* Existe o risco de interromper serviços importantes? - com as opções de "Sim" ou "Não"

* Existe um risco de perda financeira? - com as opções "Sim" ou "Não"

* Existe um risco de imagem? - com as opções "Sim" ou "Não"

Será então apresentada uma representação do risco de 0 a 100.

### Planejamento

Para planejar a mudança, use as funcionalidades:

|Guia|Descrição|
|-|-|
|Atividades|Criar um workspace ou vincular um já existente|
|Datas|Data para planejar a mudança: no campo "Data prevista de início", a data de início do planejamento deve ser indicada. No campo "Data prevista de término", a data final do planejamento deve ser indicada. Depois de indicar a data de início e a data de término, você pode verificar os conflitos clicando em "Ver conflitos". Aprovação: "Data de aceitação" must be given a date to be accepted, "Voting" must be given the date for voting, "Conclusion date" must be given a date for completion|
|Actions|Add an action for the change|
|System notifications|Set up a system notification to inform you of the change|
|Documents|Link knowledge to change|
|Attachments|Insert attachments to change|
|Annotations|Add relevant notations for change|

[Activities of the change planning phase](/en-us/4biz-helium/processes/change/use/change-planning-activities.html)

5. It's also necessary to indicate the preliminary information of "planning", "reversion plan" and "review and closure".

### Reversion plan

To plan the change reversal use the features:

|Tabs|Description|
|-|-|
|Activities | Create a Workspace or link an existing one|
|Actions | Add an action for the change|
|System notifications|Set up a system notification to inform you of the change rollback plan|
|Documents|Link knowledge to the reversal plan|
|Attachments|Insert attachments to the reversal plan|
|Annotations|Add relevant notations to the reversal plan|

[Register reversion plan of change](/en-us/4biz-helium/processes/change/use/change-reversion-plan.html)

### Review and closure

To review and finish the change, use the features:

|Tabs|Description|
|-|-|
|Revision|Informe for final User about risk analysis and impact of change|
|Activities|Create a Workspace or link an existing one|
|Incidents|Link an incident to review|
|Problems|Link an incident to a review|
|Lesons Learned|Link knowledge to the reversal plan|
|Closure|Identify the closure of a change|
|Attachments|Insert attachments|
|Annotations|Add relevant notations|

5. Click on "Options" and then on "Save”;

## Relationships

### CI of change

To link a configuration item, select Cis of the Change > Search Configuration Item, and select the configuration item.

[Relate items to the change](/en-us/4biz-helium/processes/change/use/relate-information-to-change.html)

### Service of the Change    

To link a Service of Change, select Services of the Change > Add Service, and select the configuration item.

### Questionnaires

It's not mandatory, but some changes may come along with a questionnaire. It can be used to make a survey (assessment), questionnaires can be answered and the answers will be linked to the change. The questionnaire must be created beforehand.

### Roles and responsibilities

To define the roles and responsibilities of the change, complete the fields:

|Fields|Descriptions|
|-|-|
|Employee|Username|
|Role|Role that the user will perform|
|Responsibilities|Select the responsibility to be linked to the user|

### RFC Voting

The change team can view the voting score for approval of the change.

[Approve change](/en-us/4biz-helium/processes/change/use/change-approval.html)

### Release

To link a release to a change, search for an existing one in "Search for title" or create a new release using the "Register" option

### Problem

To link a problem to a change, search for an existing one in "Search for title" or create a new release using the "Register" option

### Knowledge Base

To link a knowledge base to change, search for an existing one in "Search for title" or create a new release using the "Register" option

### Ticket

To link a Ticket to change, search for an existing one in "Search for title" or create a new release using the "Register" option

## History and Audit

To see all the actions and audits took in the Change.

## Change Schedule

Authorized production and viewing of Change schedules, For example, build, testing, and implementation schedules view all scheduled changes in the Periodic Activities Schedule and could be used as whiteboard communication methods


Relacionado 
---------------

[Criar um portfólio de mudança](/pt-br/4biz-helium/processes/change/configuration/change-portfolio.html)

!!! tip "About"

    <b>Product/Version:</b> 4biz | Helium &nbsp;&nbsp;
    <b>Updated:</b>01/31/2019 – Larissa Lourenço

