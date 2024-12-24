#📊 What is RFM Analysis?
  
  RFM (Recency, Frequency, Monetary) analysis is a marketing technique used to segment customers based on their purchasing behavior. It helps businesses identify their best customers, loyal clients, and customers    who may be at risk of churning.

🔍 Key Concepts:

#Recency (R):
  How recently a customer made a purchase.
  Lower recency values indicate more recent activity, which is good.

#Frequency (F):
  How often a customer makes purchases.
  Higher frequency suggests loyal and engaged customers.


#📁 About the Datasets:

You have two datasets with the same structure but covering different time periods:

Dataset 1:

  Time Period: 2009-2010
  
  Columns:  ['Invoice', 'StockCode', 'Description', 'Quantity', 'InvoiceDate', 'Price', 'Customer ID', 'Country']

Dataset 2:

  Time Period: 2010-2011
  Columns:['Invoice', 'StockCode', 'Description', 'Quantity', 'InvoiceDate', 'Price', 'Customer ID', 'Country']

🛠️ Steps in the Project:

Data Loading & Merging: Read both datasets and combine them for a complete view of customer transactions.

Data Cleaning: Handle missing values (dropna), filter negative quantities (returns), and ensure proper date formatting.

Feature Engineering: Calculate total purchase value (Quantity * Price). Use InvoiceDate to calculate recency.

RFM Calculation: Group by Customer ID and calculate:
  Recency – Days since the last purchase.
  Frequency – Number of transactions.
  Monetary – Total spending.

Scoring and Segmentation: Use quartiles to assign scores (1 to 4). Combine scores to segment customers (e.g., Best Customers, Lost Customers).

Visualization: Bar charts to visualize customer distribution by segment.

Monetary (M):
  How much money the customer has spent.
  Higher monetary values indicate valuable customers.
