Title: Financial Cost Calculation
Description:

# Financial Cost Calculation

1 - Access the main menu Processes > Financial Management > Financial Cost Calculation

2 - In the Financial Cost Calculation main screen, we have the following actions available:

|Action|Description|
|------|-----------|
|New| To create a new financial cost calculation|
|Generate CSV report| To generate a report of CSV|
|Advanced Filters| To set the filters to finda a cost calculation already created|
|Edit| Once selected a cost calculation already created, this option will appear to edit it|
|Remove| Once selected a cost calculation already created, this option will appear to remove it|

## Registering/Editing Financial Cost Calculation

1 - To create a new cost calculation, click on "New";

2 - To edit a cost calculation already created, search for it, click on it and then on "Edit";

3 - Complete the fields available:

|Field|Description|
|-----|-----------|
|Start date(\*)| The start date for the cost calculation|
|End date(\*)|The date to finish the cost calculation|
|Service(\*)|Select the service you want to make the cost planning|
|Minimum rate(\*)|Set a value for the minimum rate|
|Forecast(\*)|Select to forecast the cost|

(\*) Indicate mandatory fields

!!! abstract "NOTA"

    Select the start date and end date to make the 12-month Plan.
    
4 - After complete the fields, click on "Generate" to present the values. It'll generate three tabs for values information:

### Calculation of NPV and IRR

Based on the information added in the "Financial Item" functionality, the tool will present the values according to the information and calculation presented in the fields:

|Field|Description|
|-----|-----------|
|Month|The month of reference to present the costs|
|Investment|The value of investment|
|Revenue|The value of the revenue|
|Cost/Expense|The value of cost/expense|
|Result|The value of result|
|Present Value|The present value|
|Net present value| The net present value|
|Internal rate of return|The value for internal rate of return|

### Cost by Category

This tab presents the appropriation of costs by categories. The categories are: Investments and Cost distribution.

**Investments**

|Field|Description|
|-----|-----------|
|Category|The category of the distributed cost|
|Scenario variation|The percentage for the variation of scenario|
|Cost|The fixed cost number|
|%|The percentage reached|
|Total|The final value of the investment|

**Cost distribution**

|Field|Description|
|-----|-----------|
|Category|The category of the distributed cost|
|Scenario variation|The percentage for the variation of scenario|
|Cost|The fixed cost number|
|Cost breakdown|The breakdown cost|

Then, at the end of the tape, we'll have the information about: **Number of months, Investment apportionment per month, Average cost per month and Total cost per month**

### Set Price

Complete the fields available to set the prices. In the "How to price" field, select how to make the price, the options available are: Fixed value, Variable value or Both.

If you select the **Fixed value** option, complete the fields:

|Field|Description|
|-----|-----------|
|% Profit margin|Set the margin you want to work with|
|Cost|Set the fixed cost|
|Final price|The final price for the fixed value|

If you select the **Variable value** option, complete the fields:

|Field|Description|
|-----|-----------|
|What is the unit of measurement|Set the unit of measurement|
|Estimated quantity|Set the amount|
|Do you accpet less than expected quantity?|Select if you accept it or not|
|Monthly unit value|Once completed all values in the previous fields, it'll appear the monthly unit value, with the information of: % Profit margin, Cost and Final Unit Price|
|How to calculate the amounth monthly|Select how the calculation will be made: Informed manually or Automoatically calculated|
|Integration flow of quantity capture|It's where the monthly calculation will get the results|

For the **Both** option, it's possible to set a fixed cost for some cases and, if the number is not reache, it's possible to use variables costs.


