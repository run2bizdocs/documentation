title: Create time of attendance
Description: Provides a variety of actions, such as including, changing, and deleting the time of attendance of type Global (applicable to all services), Client (applicable to the contract services) and Incident/Request/Procedure (applicable to a specific service).
# Create time of attendance

This feature provides a variety of actions, such as including, changing, and 
deleting the time of attendance of type *Global* (applicable to all services), 
*Client* (applicable to the contract services) and *Incident/Request/Procedure* 
(applicable to a specific service).

Before getting started
--------------------------

To register a time of attendance, it's necessary to previously register the
service portfolio.

The configurations of the Gold, Silver, and other SLAs will be created here.

Procedure
-------------

1.  Access the functionality Time of Attendance through the main menu Processes \> Service Level Management \> Attendance Time;

2. Set the type of attendance time and click on the corresponding tab; 
   
   |Tabs|Description|
   |-|-|
   |Global|For a global use the time of attendance, without specific "Unit" or "Employee"|
   |Client|For a client use this time attendance|
   |Specific|For a Specific service use this time attendance|

3.  Complete all mandatory field in **Basic Data**;

| Fields | Description |
| - | - |
| Title | Title of identification of the SLA |
| Status | Status between "Active" or "Inactive" |
| Impact | Define the SLA impact between "High", "Low" and "Medium" |
| Urgency | Define the urgency of the SLA between "High", "Low" and "Medium" |
| Change impact / Urgency | Inform if the impact or urgency involves a change |
| Seasonal | Select if this SLA will be used of time in time |
| Start date | Set the start date of validate SLA |
| End date | Set the end date of SLA |
| Evaluates in | Set the date to evaluate this SLA |
| Description | Add a relevant description for using the SLA |
| Scope | Add a scope to the SLA |
| Contacts | Add a contact for the SLA |
| Time of Attendance by Priority | set the service time of attendance, taking into consideration the priority. The priority is used to identify the time required to an action to be taken. The priority goes from 1 to 5, being 1 the highest priority and 5 the lowest. Select the priority to define the time: ** Capture **: set the time of capture of the service request, according to the priority selected; ** Resolution **: set the time of service resolution according to the priority selected. |
| Hour | Enter the SLA "capture" and "Resolution" time |
| Minute | Enter SLA "capture" and "Resolution" minutes |

4.  Before complete the fields in **Automation**, it should be properly
    parametrized, it must be properly parameterized, so it is necessary to
    execute the steps in the knowledge Creation escalation rule, except for
    parameter 190 that must be equal to 'N' in this context;

| Fields | Description |
| - | - |
| Automation ||
| Time of Action | Time after a scenario is true for the execution of an automatic action |
| Email Template | One of the actions is sending email to a group |
| Priority | The new priority that the service that will be scheduled will receive; |
| Group | Group to whom the assistance will be directed after the scheduling action;
| Target | SLA focus / target |
| Unit (only for Client and Specific) | Unit for using the SLA |
| Employee (Only for Client and Specific) | Employee with permission to use the SLA |
| Requester´s Group (Only for Client and Specific) | Requesting group which will be linked to the SLA |


    !!! Abstract "IMPORTANT"

        Indicate in the attribute "Impact/Urgency Change", if it'll be allowed the 
        change of Impact and/or Urgency.
        
    !!! Abstract "ATTENTION"
    
        If the attendance time does not allow the change of impact and urgency, the 
        system automatically replaces what is sent via WebService to the impact, 
        urgency, priority and time of attendance defined in this register.



5.  Before the N minutes (informed in the time of action) and in case it doesn't
    have performed any action in the service request linked to this time of
    attendance, the system will attribute the priority and will escalate the
    execution group to the service request;

6.  In the fields of **Incident/Request/Procedure**, it will be selected the
    services to apply the configurations, taking into consideration the type of
    attendance time selected;

7.  Click on "Save".


Related
-------

[Register a service](/en-us/4biz-helium/processes/portfolio-and-catalog/use/register-a-service.html)

[Configure service attributes](/en-us/4biz-helium/processes/portfolio-and-catalog/use/configure-services-attributes.html)

[Create the portfolio](/en-us/4biz-helium/processes/portfolio-and-catalog/use/create-the-portfolio.html)

[Configure parametrization – ticket](/en-us/4biz-helium/platform-administration/parameters-list/configure-parametrization-ticket.html)

[Create escalation rule](/en-us/4biz-helium/processes/tickets/use/create-escalation-rule.html)


<i class='fa fa-youtube-play  fa-2x' style='color:#97ce17;vertical-align: middle;'> </i> [Video Library](https://www.youtube.com/playlist?list=PLB5qK2uzf2RMDKjZH8augISpB17EQqrrc)'

!!! tip "About"

    <b>Product/Version:</b> 4biz | Helium &nbsp;&nbsp;
    <b>Updated:</b>01/04/2019 - Anna Martins
