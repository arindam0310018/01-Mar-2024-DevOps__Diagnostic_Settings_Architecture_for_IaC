# Diagnostic Settings Architecture for IaC:-

Greetings to my fellow Technology Advocates and Specialists.

In this Session, I will explain and showcase - __Diagnostic Settings Architecture for IaC__.

| __DISCLAIMER:-__ |
| --------- |
| In this Article, I am __NOT__ covering Diagnostic Settings Architecture of all available Azure Services but the ones which I have worked upon. |
| __From the below code repository, please download the excel sheet named "Azure-Diagonostic-Settings-Architecture-v1.0.xlsx" which details the Diagnostic settings of each Azure Services, I have worked upon and the destination where it should be shipped to.__ |

| __SAMPLE SCREENSHOT: HOW THE ARCHITECTURE MATRIX LOOKS:-__ |
| --------- |
|  |

Each Azure Services may or may not have Diagnostic settings. Diagnostic settings indicates that which logs will be shipped to which destination.

| __WHY DIAGNOSTIC SETTINGS ARCHITECTURE IS IMPORTANT:-__ |
| --------- |

| __#__ | __POINTERS__ |
| --------- | --------- |
| 1. | Logs can be related to Infrastructure, Application, Database and Security. So Proper segregation is required for daily operations. |
| 2.  | If all logs are pushed to same Log Analytics workspace, we cannot bifurcate the cost per domain/application. |
| 3. | A clear definition will help establish, as which logs, we want to push to log Analytics and which one, we would like to archive in Storage Account as Log Analytics can be very expensive very fast if not defined properly. |
| 4. | This clear definition can then be replicated for all projects to keep it consistent organisation wide (We all know it is always not possible but to the extent we can :-)) which can eventually become one of the best practices. |
| 5. | This definition can then serve as a blueprint for IaC (Infra-As-Code). |

| __WHERE LOGS CAN BE SHIPPED:-__ |
| --------- |
| 1. Send to Log Analytics workspace. |
| 2. Archive to a storage account. |
| 3. Stream to an event hub. |

Below table indicates the list of Azure Services for which this Diagnostic Settings Architecture is applicable.

| __#__ | __AZURE SERVICES WITH DIAGNOSTIC SETTINGS__ |  __TOTAL COUNT OF AZURE SERVICES__ |
| --------- | --------- |  --------- |
| 1. | Virtual network, Network Security Group, Route table, Private Endpoint, Network Interface, DNS Zone, Private DNS Zone, Load balancer, Public IP Address, Virtual network gateway, Local network gateway, Managed Identity, Key Vault, App Service Plan, App Service, Function App, Application Insights, API Management, Application Gateway WAF Policy, Application Gateway, Proximity Placement Group, Virtual machine, Disk, SQL Server, SQL Database, SQL elastic pool, Azure Database for MYSQL single server, Azure Database for PostgreSQL flexible server, Azure Database for PostgreSQL single server, Azure Cosmos DB account, Azure Cosmos DB for PostgreSQL Cluster, Azure Cosmos DB for MongoDB account (RU), Data Factory (V2), Microsoft Purview account, Azure Synapse Analytics, Azure Databricks Service, HDInsight cluster, Kubernetes Service, Azure Cache for Redis, Service Bus Namespace, Event Grid Domain, Event Grid System Topic, Logic App, B2C Tenant, Twilio Sendgrid, Elastic, Azure AI services, Search Service, Azure Managed Grafana |  49 |

You will be surprised to know that there are a lot of Azure Services which __DOES NOT__ have Diagnostic Settings option. 

Below follows the List -

| __#__ | __AZURE SERVICES WITHOUT DIAGNOSTIC SETTINGS__ |  __TOTAL COUNT OF AZURE SERVICES__ |
| --------- | --------- |  --------- |
| 1. | Route table, Private Endpoint, DNS Zone, Private DNS Zone, Load balancer, Virtual network gateway, Local network gateway, Managed Identity, Application Insights, Application Gateway WAF Policy, Proximity Placement Group, Disk, SQL Server, Azure Cosmos DB account, Azure Databricks Service, B2C Tenant, Twilio Sendgrid, Elastic, Azure AI services |  19 |

__Hope You Enjoyed the Session !!!__

__Stay Safe | Keep Learning | Spread Knowledge__
