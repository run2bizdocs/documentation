Title: Store information in dialogues
# Store information in dialogues

Many times, the user during a dialogue, provides us information that will be used at another time for a better understanding of the user's interest. Helper recognizes this information as Contexts.

In a conversation, for example, in which the user requests that Helper inform which Italian restaurants exist within 10 km distance, we can have three contexts: type of establishment, category and distance.

In this case, we create Contexts that are able to store this information to respond more accurately to the user.

Contexts types define the format of the information that can be saved in it. Helper works with the following types:

 - Text slot: where you can add text-type values;

 - Boolean slot: used for values that are set to true or false;

 - Categorical slot: used to store a value from a predefined list;

 - Float slot: where we can add numerical values with minimum and maximum limits.


!!! Abstract "NOTE"
    
    Tt would not be possible to create interest that represented all possible combinations 
    for the three information. In this case the ideal would be to use the contexts.


Procedure
------------
1. Access the menu “Contexts”;

2.	Click on “New”;

3.	Complete the name and type of the context;

4.	Enter the other required fields according to the type and click on "Save".
