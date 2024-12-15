# CIS731-finalproject
Final Deliverables for CIS731 Final Project

The dataset utilized in the project is the "Online Retail" dataset from UC Irvine Machine Learning Repository, https://archive.ics.uci.edu/dataset/352/online+retail.
The dataset was acquired from the Databricks Solution Accelerator, found here: https://www.databricks.com/solutions/accelerators/customer-lifetime-value. 

Many of the cleaning steps follow the Databricks Solution Accelerator. Cleaning required of the dataset includes: 
- Changing InvoiceDate from a string data type to a Date data type
- Create Sales column: Quantity * UnitPrice
- Some cleaning required, including removal of null CustomerID, customers with extremely large daily purchases (+70,000 in 1 day)
- Utilize PySpark functions like WithColumn, filter
- Calculating various metrics for each unique CustomerID:
    Recency: time since last purchase,
    Frequency: number of unique invoices,
    Monetary Value: how much each customer spends
- Scale data using MinMaxScaler
- Create vector of scaled and unscaled RFM features using VectorAssembler for use in clustering and classification
- Split data into train and test sets (70/30)

More specific cleaning steps and preparation for ML modeling can be found in the writeup and presentation files.

