Title: How to interact Helper with other systems
# How to interact Helper with other systems

In order for Helper to interact with other systems, it is necessary to add a custom ability in the dialog. 

The query is made through a Rest API, which must be made available by the system that holds information of interest to the user. Eg.: search for information on the status of a ticket, creation of tickets, generation of bills in the system.

Procedure
-----------

1. Access the menu “Dialogs” and click on “New”;

2. Complete the information of the **Interest** section;

3. In the **Ability** section, select the type *Customized*;

4. Complete API Section information, including body example and response;

5. If necessary, enter the heading;

6. In the Answers section, we have two action options:


    a) Answers in memory: In this case, the value returned by the API is associated with the selected attribute;
 
    b) Answers in text: Returns a text message to the user.

7. If it's necessary to forget a context, in the Forget Value field, it's possible to delete the information in the bot's memory, so that the chatbot doesn't use this value at another time
  
!!! Abstract "NOTE"

    The integration needs to be homologated by 4biz, so after setting up this skill, you need 
    to open a ticket for us to do the homologation of the integration.
   
