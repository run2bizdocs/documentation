Title: Implementing 4biz Inventory

# Implementing 4biz Inventory

4biz Inventory is a component of the 4biz Platform that enables you to collect, register and manage information from IT assets. It enables you to manage the lifecycle of your organization's configuration items from the Configuration Management process.  

![Architecture INV and EVM](images/cloud-arch-inv-evm.png)

## Before getting started

- [x] 4biz Inventory works together with [4biz Event Monitor - EVM][1] as a data collector (eg.: XML packages), and EVM serves as repositories for this information. Therefore, to enable the Inventory, you must first configure the EVM.  


## Procedure

1. [Install][2] the Wildfly application server;
2. Download the WAR package from the EVM component;  
3. Unpack the files;  
4. Copy the package to the deployment folder of the Wildfly application server;  
5. Configure [System Properties][3] with data of 4biz instance;

## What to do next

To test the Inventory, [configure][4] the connections in the 4biz instance.

## Related

[Implement 4biz Event Monitor][5]

[Asset and Configuration Management][6]


[1]:/en-us/4biz-helium/additional-features/add-ons/event-monitor.html
[2]:/en-us/4biz-helium/get-started/installation-and-upgrade/perform-installation.html
[3]:/en-us/4biz-helium/get-started/installation-and-upgrade/perform-installation.html#configure-system-properties
[4]:/en-us/4biz-helium/processes/event/configuration/set-inventory-connection.html
[5]:/en-us/4biz-helium/additional-features/add-ons/event-monitor.html
[6]:/en-us/4biz-helium/processes/configuration/overview.html
