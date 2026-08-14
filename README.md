# Notes
## Attendance Daily Report

- Download the file
    - Details only
    - Format as .csv
- Clean the data
    - All date -> Data(Ribbon) -> Text to column -> MDY
    - Store code -> Make the data type **"Number"**
    - Add the column se;;et **Seller name**, **OM**, **Banner**
## NOTE: LOCK ALL THE COLUMN OF BASE OR RANGE COLUMN (STORE CODE)



## 

## Tracking report
- Download the file (Promotion Tracking Report) like you download the Attendance report
- Clean the data  like you clean the attendance report
- Add column **Seller name**, **OM**, **Banner**
    - Populate the columns you add from mdm using **Vlook up**
- Add **Concat**  column
    - concatinate the **store code** and **siebel** and **visited date**
    - Add the column **Unique** and populate using **CountIf**
    - **Countif** the **Concatinated** data
- Clean the **Unique** column data
    - FIlter -> Sort to largest to smallest
    - Filter **N/A** if there's  **N/A** and delete all the ROW
    - Filter and select 4 or the largest to smallest 
    - if 4 just make the first row 1 and delete or
        make the 3 4's down blank and copy the first 4 row and paste it in entire column
    - make that step to all the numbers in filrter except 1
    - if done delete the concatinated column and save


## NOTE: BEFORE SAVING ERASE ALL THE FUNCTIONS AND FILTER
    
##

## MISSING PSKU
- Download the file
    - Clean the data (Visited date)
- Add the column
    - Local site Key - 2
    - Store name - Site Name - 9
    - ROIC - Sellet Name - 4
    - OM - 5
    - Local Store Banner - Local Store Banner Name - 10
- Add A Pivot Table
    - Select all the column and row
    - Add a pivot table (insert (RIBBON)), Select pivot table
    from table range
    - Add the local site key in rows
    - Add the visit date to the values and make it 
- Add concat column and latest column
    - concat the local site key and max of visit date
    - Add **"Latest"** in latest column
    - Copy the column and paste it in entire column
- Go to raw data and add the concat and latest column
    - Concat the local site key and visited Date
    - **VlookUp** the latest and make the range of concatinated date and go to pivot table and selsect the concatinated, and latest column and put the number or column that you want to appear in latest column in you data sheet which is 2
    - always lock the criteria
- Create pivot table again
    - Put the local site key, **product: barcode text**, **product: category** in row
    - Go to **Design** **(RIBBON)** the **report layout**, **show in tabular**, repeat all item labels
    - Select **Subtotal (RIBBON)** -> **Do not show subtotal**
- Add the concat and true of false column
    - Concat the **local site key, product:barcode text, product: category** and add the value of true of false column by inserting 1 in first column
    - Copy the concatinate data and the true of false column and paste it in entire date
    - Create and concat column again and this time concatinate the **Local site key, product code category**
    - Create look up column and **Vlookup** the concatinated data from mapper and the concatinated data and the true of false column and make the return value as true of false and lock the criteria
    - Copy the concatinated data from mapper to missing psku raw
    - populate the **store name, roic, om local store banner** and get the data from **MDM**
    - Populate product:barcode, product:category, product:brand and local site key by creating data to mapper.
    - the column **store code and name** - concat the **locala site key and store name**

## NOTE: MAPPER DATA FETCHING
- Local site key - 2
- product: varcode - 3
- product: Category - 4
- product: product name - 6

## MDM DATA FETCHING
- open the PE result
    - Concat product code and category 
    - Filter the question to **Distributed**
## Open the missing psku raw
#
- Concat the product code and category
- **Vlookup** the visit date to PE file
- Filter the **N/A's** and delete
- Filter the 1900's years and delete the value and add 1 to target column and missing **PSKU**
- Filter again the  date visited and select the **Current month** and add to **status**(Distributed), column **target** (1), column **Distributed** (1)