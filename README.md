# Aging Balance Report based on SAP and Salesforce Data
The aim of this project is to create a clear and compact report that combines customers overdues data from Salesforce and SAP for data analysis purposes.
### Tools used
The report was created using Power Query Editor and standard Excel tools such as functions and data formatting.
### Source Data 

| Dataset     | Data Description                                                   | Example Columns                              |
|----------------|---------------------------------------------------------------------|---------------------------------------------------|
| SAP            | Contains accounting records exported from SAP ERP system. Includes customer transactions, invoices, due dates, and payment statuses. | CustomerID (string), InvoiceDate (date), DueDate (date), Amount (float), PaymentStatus (string) |
| Salesforce (SF)| Contains customers master data exported from Salesforce CRM. | AccountID (string), AccountName (string), Banding (string),         |

The data was imported to the PowerQuery editor in the CSV format.
## Data Transformation with Power Query
The approach used in this project was duplicating the SAP data, grouping and merging with SF data by the AccountID key. Step by step process goes as following 
1. duplication of the SAP data as a separate Table
2. removal of unnecessary columns from the Table
3. Addition of the buckets based on the arrears column
4. Grouping by the AccountID
5. Joining the SF data and removing unnecessary columns
6. Adjustment of the headers and column order

![]([PowerQuerySS.png)
