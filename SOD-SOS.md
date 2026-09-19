# NOTE
## SOS and SOD NOTES

### SOD duration 
- Every 15 Days
- File have a million columns so download the files every 5 days duration then combine it into 1 file,

### PROCEDURE HOW TO CREATE SOD REPORT
 #### DOWNLOAD :
- First download the file **MASA -> Copy - VGP SOD w Display Type**
- FIlter the **Visit date** in SFDC when you download the file since 15 days that the report needs, filter it 5 days per file coz this file is to large ***(a million colums)***
- Look at the filtered date in these 3 Pictures.
![alt text](src/images/sodAndSos/image-1.png)
![alt text](src/images/sodAndSos/image-2.png)
![alt text](src/images/sodAndSos/image-3.png)

#### CREATION :
- Remove the Dummy in column ***Market Measure Master: Name***
![alt text](src/images/sodAndSos/image-5.png)
- Select all ***Dummy*** and **Delete the Row**
![alt text](src/images/sodAndSos/image-8.png)
- Dummy Deleted
![alt text](src/images/sodAndSos/image-9.png)
- Clean the data "Visit Date, Store codes"
![alt text](src/images/sodAndSos/image-6.png)
- After Cleaning 
![alt text](src/images/sodAndSos/image-7.png)
- After cleaning. make sure to look for the visit date and make sure that the only month there is the current month and the day is the day that you filter in SFDC
![alt text](src/images/sodAndSos/image-11.png)
- Next Create 2 columns **Seller name and OM** and populate the data from MDM using the ***Store code*** that **raw data** provided
![alt text](src/images/sodAndSos/image-10.png)
- After populate the columns, see the N/A **NOTE: the N/As means the outlet is not our account**
- Select all the columns and row and Create a **Pivot table** to get a **Latest**
![alt text](src/images/sodAndSos/image-12.png)
- Inside the pivot table display the **STORE CODE, Product Category: Product Hierarchy Name, Standard List Master : List Name. and VISIT DATE**
![alt text](src/images/sodAndSos/image-13.png)
- then create a **Concatinate, Latest column** then concat the **STORE CODE, Product Category: Product Hierarchy Name, Standard List Master : List Name. and VISIT DATE**
![alt text](src/images/sodAndSos/image-14.png)
- Go back to the Raw data and create **Concatinate, Latest column**
![alt text](src/images/sodAndSos/image-15.png) 
- Then Concat the column **STORE CODE, Product Category: Product Hierarchy Name, Standard List Master : List Name. and VISIT DATE** to get the Latest value
![alt text](src/images/sodAndSos/image-16.png)
- After that ***Vlookup*** the Latest column with the **Created Pivot**
![alt text](src/images/sodAndSos/image-17.png)
![alt text](src/images/sodAndSos/image-18.png)
- after that Look for the N/As NOTE: Why reason there's a N/As coz that account is not one of our account. and Just delete it
![alt text](src/images/sodAndSos/image-19.png)
![alt text](src/images/sodAndSos/image-20.png)
- after you deleted the N/As just copy all the data into work sheet that you will paste all the clean data from the 3 files you downloaded from SFDC