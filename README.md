# LogiConf19Training
This app has been developed to be a reference in the 2019 Logi Conference. The Conference includes 25 hours of in-depth presentations by solution architects, web developers, support engineers, professional services consultants, and product managers.

## Getting Started
### 1. Prerequisites
1.1. Having the [IIS configured](https://documentation.logianalytics.com/logiinfov12/content/installing-logi-info-on-windows-10.htm).

1.2. Having [Logi Info Studio 12.6.089](https://documentation.logianalytics.com/logiinfov12/content/installing-logi-info-on-windows-10.htm) installed.

1.3. Having the Microsoft SQL Server Management Studio installed.

1.4. Having a user created in the sql server database, the user credentials are the ones used inside the logi **_Settings** file, inside the applicatoin you are going to create in a while.

### 2. Setting-up the Application
2.1. Create a new blank Logi application:

* Run logi info studio as administrator.
* From home tab , click on **New Application**.
* Select **Microsoft.Net** as the type of the application.
* Use **logiConf2019_Training** as the name of the application, please make sure you use the exact name.

2.2. Setting up the logi application from the training repository:
* Clone the **LogiConf19Training** repository from github into any place in your machine.
* The repository contains three folders, **logiConf2019_Training,Embedded_analytics_html,security_embedded**:
  * Copy the two folders **Embedded_analytics_html,security_embedded** into **C:\inetpub\wwwroot**
  * Copy all the contents inside the folder **logiConf2019_Training** into **C:\inetpub\wwwroot\logiConf2019_Training**, This will overwrite the existing folders **_Definitions** and **_SupportFiles** in the blank logi application that we created in step 2.

2.4. Create **export** and **exportCompressed** folders inside **logiConf2019_Training** application folder, and give them **Full control** permission.

2.5. Register the **security_embedded** app in IIS.  

### 3. Setting-up the used databases
3.1. Install the [AdventureWorks2016CTP3.bak](https://www.microsoft.com/en-us/download/details.aspx?id=49502) file.

3.2. Install the [AdventureWorksDW2017.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2017.bak) file.

3.3. Install the [AdventureWorks2017.bak](https://github.com/microsoft/sql-server-samples/releases) file.

3.4. Restore 'AdventureWorks2016CTP3.bak', 'AdventureWorksDW2017.bak', and 'AdventureWorks2017.bak' files.

### 4. Adding tables within their data to AdventureWorks2016CTP3 database, by executing [this script.](https://gist.github.com/SSukkar/ebac833504f28d27495baeda25783c49)
