title: Registering a change
Description: It's intended to register a change.

# Registering a change

This functionality is intended to register a change. According to ITIL, it's necessary to formalize the change request, so that the responsible team registers all the procedures performed for the change you want (from its request to the impact of its implementation), monitoring it throughout its lifecycle.


Before getting started
------------------


In order to register a change, it's necessary to previously register a contract, a unit that it is linked to the contract, an employee, a questionnaire, the Change Advisory Board, have a group linked to the contract associated with the Requesters (employees) already registered to this group. If it's necessary to create a new employee, it's necessary to include it in the Requester Group in which it's related to the contract.
Moreover, it's necessary to have registered the portfolio of changes.


Procedure
--------------
1.    Access the main menu Processes > Change Management > Change;
2.    Click on "Options" and then on "Register";
3.    Complete the fields available:


### Identify the requester

To identify an applicant, fill in the fields:

|Fields|Description|
|---|---|
|Name (\*)|Requester's full name|
|Contact (\*)|Indentify the user's contact|
|Email (\*)|User's email|
|Phone|User's phone number|
|Extension|The extension number of user|
|Unit (\*)|User's unit|
|Phisical Location|User's Physical Location|
|Other information|Additional user's information|

### Identify the change

To identify a change, complete the fields:

|Fields|Description|
|---|---|
|Title (\*)|Title identifying the change|
|Change description (\*)|Description of change|
|Effect of not implementing the change|Effective if this change is not implemented |
|Contract|Contract linked to change|
|Importance|Importance level of change|
|Impact|Impact that change generates|
|Urgency|Urgency to make the change|
|Executor Group|The group responsible for executing the change|
|Notification|Configure notifications between "Send email upon creating the Change", "Send email on the completion of the Change", "Send an Email to the Change Advisory Board", "Send email for other actions of the Change"|

### Plan the change

To plan the change use the features:

|Tabs|Description|
|-|-|
|Activities|Create a Workspace or link an existing one|
|Date|Date for planning the change: In the "Expected start date" field, the start date of the planning must be indicated. In the "Expected end date" field, the end date of the planning must be indicated. After indicating the start date and end date, you can check the conflicts by clicking on "View conflicts". Approval: "Acceptance date" must be given a date to be accepted, "Voting" must be given the date for voting, "Conclusion date" must be given a date for completion|
|Actions|Add an action for the change|
|System notifications|Set up a system notification to inform you of the change|
|Documents|Link knowledge to change|
|Attachments|Insert attachments to change|
|Annotations|Add relevant notations for change|

5. It's also necessary to indicate the preliminary information of "planning", "reversion plan" and "review and closure".

### Create a reversal plan

To plan the change reversal use the features:

|Tabs|Description|
|-|-|
|Activities | Create a Workspace or link an existing one|
|Actions | Add an action for the change|
|System notifications|Set up a system notification to inform you of the change rollback plan|
|Documents|Link knowledge to the reversal plan|
|Attachments|Insert attachments to the reversal plan|
|Annotations|Add relevant notations to the reversal plan|


### Review and finish the change

To review and finish the change, use the features:

|Tabs|Description|
|-|-|
|Revision|inform if the change was successful|
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

### Moving services

To link a Service of Change, select Services of the Change > Add Service, and select the configuration item.

### Answering Questionnaires

It's not mandatory, but some changes may come along with a questionnaire. It can be used to make a survey (assessment), questionnaires can be answered and the answers will be linked to the change. The questionnaire must be created beforehand.

### Define roles and responsibilities

To define the roles and responsibilities of the change, complete the fields:

|Fields|Descriptions|
|-|-|
|Employee|Username|
|Role|Role that the user will perform|
|Responsibilities|Select the responsibility to be linked to the user|

### RFC Voting

The change team can view the voting score for approval of the change.

### Link a Release

To link a release to a change, search for an existing one in "Search for title" or create a new release using the "Register" option

### Link a Problem

To link a problem to a change, search for an existing one in "Search for title" or create a new release using the "Register" option

### Link a Knowledge Base

To link a knowledge base to change, search for an existing one in "Search for title" or create a new release using the "Register" option

### Link a Ticket

To link a Ticket to change, search for an existing one in "Search for title" or create a new release using the "Register" option

## History and Audit

To see all the actions and audits took in the Change.

Related 
---------------

[Create portfolio of change](/en-us/4biz-helium/processes/change/configuration/change-portfolio.html)

!!! tip "About"

    <b>Product/Version:</b> 4biz | Helium &nbsp;&nbsp;


