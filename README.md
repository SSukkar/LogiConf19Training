# LogiConf19Training
This app has been developed to be a reference in the 2019 Logi Conference. The Conference includes 25 hours of in-depth presentations by solution architects, web developers, support engineers, professional services consultants, and product managers.

## Getting Started
### 1. Prerequisites
* [.NET Framework](https://documentation.logianalytics.com/logiinfov12/content/installing-logi-info-on-windows-10.htm) : Logi products require the .NET Framework components. When Windows is installed, multiple versions of the framework are typically included. Before doing anything else, ensure that you have .NET installed by using File Explorer to browse to:

**C:\Windows\Microsoft.NET\Framework**
where you should see several folders, such as v4.0.30319, one for each version of .NET installed. The .NET Framework 4.x is required. If not already in place, with your consent, appropriate versions of the .NET framework are installed when Logi products are installed. They are also available for free from the Microsoft Download Center.

* [Enable the IIS Web Server](https://documentation.logianalytics.com/logiinfov12/content/installing-logi-info-on-windows-10.htm) : this logi application requires to have the IIS installed and enabled.

* Install [Logi Info Studio 12.6.089](https://documentation.logianalytics.com/logiinfov12/content/installing-logi-info-on-windows-10.htm).

* Install Microsoft SQL Server Management Studio: this logi application requires some databases that should be imported.


### 2. Setting-up the logi Application
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
  * Inside **C:\inetpub\wwwroot\logiConf2019_Training** give the following folders a read/write permissions to allow IIS to read/write on those folders , right click on each folder > properties > Choose Security tab > Click Edit > Add IIS_IUSRS > Allow Full Control
   * rdDownload
   * rdDataCache
   * export
   * exportCompressed

2.3. Register the **security_embedded** app in IIS, open IIS > Sites > default web sites > right click on folder **security_embedded** > click convert to application.  

### 3. Setting-up the databases
3.1. Download the following databases and copy them to the backup folder under the installation path of the SQL server , ie. C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\Backup:
* [AdventureWorks2016CTP3.bak](https://www.microsoft.com/en-us/download/details.aspx?id=49502).
* [AdventureWorksDW2017.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2017.bak)
* [AdventureWorks2017.bak](https://github.com/microsoft/sql-server-samples/releases)

3.2. Restore the downloaded databses:  Open SQL Server management studio > connect to your local server > right click on databases > click on restore database > In General choose Device as the source > select backup file > click Add > search for the downloaded files in the backup foder under the installation path of the SQL server > click ok.

3.3. Run [this database script](https://gist.github.com/SSukkar/ebac833504f28d27495baeda25783c49) inside the database **AdventureWorks2016CTP3**, this will create the required menu/submenu items for the logi application **logiConf2019_Training**.
