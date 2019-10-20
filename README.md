# LogiConf19Training
This app has been developed to be a reference in the 2019 Logi Conference. The Conference includes 25 hours of in-depth presentations by solution architects, web developers, support engineers, professional services consultants, and product managers.

## Getting Started
### 1. Prerequisites
1.1. Having the [IIS configured](https://documentation.logianalytics.com/logiinfov12/content/installing-logi-info-on-windows-10.htm).

1.2. Having [Logi Info Studio 12.6.089](https://documentation.logianalytics.com/logiinfov12/content/installing-logi-info-on-windows-10.htm) installed.

1.3. Having the Microsoft SQL Server Management Studio installed.

1.4. Having a user added to the database, within credentials included in **_Settings** file.

### 2. Setting-up the Application
2.1. Create a Logi application in 'C:\inetpub\wwwroot' path.

2.2. Download the **LogiConf19Training** Repository as ZIP file in the same path.

2.3. Uncompress the **LogiConf19Training** ZIP file.

2.4. Copy the contents of **LogiConf2019_Training** and paste them in Logi app you have already created. This should override the **_Definitions** and **_SupportFiles** folders.

2.5. Register the **security_embedded** app in IIS.  

### 3. Setting-up the used databases
3.1. Install the [AdventureWorks2016CTP3.bak](https://www.microsoft.com/en-us/download/details.aspx?id=49502) file.

3.2. Install the [AdventureWorksDW2017.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2017.bak) file.

3.3. Restore 'AdventureWorks2016CTP3.bak' and 'AdventureWorksDW2017.bak' files.

### 4. Adding tables within their data to AdventureWorks2016CTP3 database, by executing [this script.](https://gist.github.com/SSukkar/ebac833504f28d27495baeda25783c49)
