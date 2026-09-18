# NOTE:
### PSKU

#### DOWNLOAD
- Download Path MASA/MASA report templates/Missing PSKU Report
- Set the duration **1 month** ***(Current month)*** 
    - **NOTE: First day of the month (ex: sept 1 up to current date)**
    ![alt text](image.png)

#### CREATION OF REPORT
- After downloading the PSKU raw, clean all the data that necessary to clean such as **Visit Date, Product barcode text** and also copy the **Store ID** and paste it in the first colomn, coz that **ID** will use to the populating Data.
    - Raw Data
    ![alt text](image-1.png)
    - After Cleaning 
    ![alt text](image-2.png)
- After that, add the necessary Data ***(Local Site Key, Store Name, ROIC, OM,  Local Store Banner, Local Store KBD Cluster Name)*** and ***populate it*** using **Store ID** to **MDM**
    - Added column
    ![alt text](image-3.png)
    - Populated
    ![alt text](image-4.png)
- After that you can add the following ***COLUMNS (Status, Target, Distributed, Missing PSKU, Count of Store, and the Latest)***
    - **NOTE: if you do the **PSKU** report all data in raw SFDC file will mark as STATUS: MISSING PSKU, TARGET: 1, DISTRIBUTED: blank, MISSING PSKU: 1. and keep the Latest column blank you will be populate that column using concat and vlookup**
    ![alt text](image-6.png)
- After that, just ***select all the columns*** and create a **PIVOT table and display Local Site Key, and Visit Date** and create a concat column and the remark column
    - ![alt text](image-8.png)
- Go back to the raw Data and create the concat column beside the column Latest, and the value of the concat column is concatinated **Local Site Key, and Visit Date** get the ***Latest*** value in ***PIVOT*** using **Vlookup** and just paste all the function to intire column
    - Getting the Latest Value 
    ![alt text](image-9.png)
    - Function pasted to entire column
    ![alt text](image-10.png)