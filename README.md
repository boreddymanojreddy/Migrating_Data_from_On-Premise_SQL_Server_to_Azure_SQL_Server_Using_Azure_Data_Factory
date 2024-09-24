# on-premise-sql-server-to-azure-sql-server
copy data from the on-premise SQL server to the Azure SQL server

![image](https://github.com/user-attachments/assets/c8e609c0-089a-415b-95d9-b51644ca90d9)
### let's get started
To get started with this project, you must have access to:
* azure subscription
* On-premise SQL server database

you will need the below resources for the on-premise sql server

* on-premise sql server(ex:Microsoft SQL server(ssms))
* SQL server authentication
* Database
* Tables

You will also need to have the following resources in your Azure Subscription created:

* Resource Group
* Azure Data Factory
* Azure DataLake Gen 2
* Azure Key Vault
* Azure SQL server/database
* SQL server firewall
* Azure SQL Server Database Instance

steps to follow:
1. open azure data factory(after launching azure studio)
2. click on author(looks like pen symbol)
3. click three dots on the pipeline tab and select new pipeline.
4. The activities page will appear, type "copy data" on the search bar and drag and drop the copy activity
5. In copy data activity select the source dataset(on-premise SQL server)
6. Select Azure sql database as sink dataset(azure sql)

  
  
