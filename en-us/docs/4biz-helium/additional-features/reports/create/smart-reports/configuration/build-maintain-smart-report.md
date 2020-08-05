title: Build and maintain smart reports
Description: Intended to customize reports with the required functionality data, without the need for new updates or additional software.
# Build and maintain smart reports

This functionality is intended to customize reports with the
required functionality data, without the need for new updates or additional
software.

Before getting started
--------------------------

- [x] It's necessary to have registered sub-reports.

Procedure
-------------

1.  Access the functionality through the main menu Reports \> Smart Reports \>
    Smart Report Creator;

2.  Click on "New";

3.  Complete the fields for "Register" and "Parameters". Define the type:

       + **SQL**: create a sub-report "SQL" (this type allows you to create reports that return the database information through a Query).          When selecting this option, it's necessary to also inform the type of report to be created, the business rule concerning it, the       report designer, the parameter and the script;  

      + **RhinoScript**: to create a report that returns the information of the Database through a "Script", it's necessary to select the         type "RhinoScript". It'll be necessary to choose the report type, define the parameters and describe the script;  

      + **JPS**: create a report with dynamic content. When opting for this type, you must inform the parameters and the "JSP" script;  

      + **Builder**: create a report of type "Builder", simply link a previously registered "Builder" form.  


    !!! Abstract "NOTE"

        To create a sub-report (Drill), the "Report Type" should be "Pie Chart"
        or "Bar Chart".  

4. Define the module (functionality) where the report being created will be
    displayed:

      +	**N/A**: select this option if you want the report not to be displayed in any module;  

      +	**General**: select this option to display the report in one or more modules, where you want the report to be displayed        (Configuration, Incidents/Requests, Incidents/Requests (chart), Release, Change, Problem);  

      +	**Specific**: select a single module where you want the report to be displayed (Configuration, Incidents/Requests,    Incidents/Requests (chart), Release, Change, Problem).  

5.  Click on "Save";

6.  There is the possibility to also import a "Report". Therefore, click on
    "Import" and link the file containing the information you want.

!!! Abstract "ATTENTION"

    The reports created here will be displayed in the "Smart Reports" screen,
    where you can view the relevant data for each report.  

Related
-------

[Emit report using Smart Report](/en-us/4biz-helium/additional-features/reports/create/smart-reports/configuration/create-smart-report.html)
