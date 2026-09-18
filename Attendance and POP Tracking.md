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
    