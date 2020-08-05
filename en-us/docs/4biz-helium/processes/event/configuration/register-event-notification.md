title: Register event notification
Description: Establish which rules will define a notification event.
# Register event notification

This functionality aims to establish which rules will define a notification
event, that is, perform the notification setting that will be triggered when the
EPL conditions are met.

It's necessary to have knowledge in the event processing language. For further
information, go to:<http://www.espertech.com/esper> .

This feature provides a variety of actions, such as including, changing, and
deleting an event notification.

Before getting started
--------------------------

- [x] To register the event notification, it's necessary to have registered the
recipient, email template, notification template and EPL template.

Procedure
-------------

1.  Access the functionality through the main menu Processes \> Event Management
    \> Business Monitor \> Notification Events Configuration;

2.  Complete the fields available in each area: Basic data, Check - EPL, Notification via Email, Notification on Screen;

3.  On the Notification on Screen area:

    * click on "Link user" to link the user to the notification on screen;

    * click on "Link group" to link group to the notification on screen.

4.  Click on "Save".


!!! Abstract "RULE"

    At the time of writing, the system does a validation of the EPL syntax.



Related
-------

[Configure email templates](/en-us/4biz-helium/platform-administration/email-settings/email-templates-configure-email-template.html)

[Register notification recipient](/en-us/4biz-helium/processes/event/configuration/register-notification-recipient.html)

[Register EPL template](/en-us/4biz-helium/processes/event/configuration/register-epl-template.html)

[Register notification template](/en-us/4biz-helium/additional-features/communication-and-notification/notification/configuration/template-create.html)
