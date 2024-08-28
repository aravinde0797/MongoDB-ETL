# ETL Transformations in MongoDB
This project explains how we can perform ETL transformations over NOSQL Databases.  Here, I have considered a sample MongoDB database "sample_analytics" (provided for learning/training purpose by MongoDB) as **Source**.  This database contains 3 collections such as accounts, customers and transactions.  Depicting the Financial application, it provides data related to details of the products purchased by the customers, list of transactions along with their account_ids and other benefits associated with it.  For Data Transformations PFB metioned **Business Logic** section.  This project primarily focuses on the "T (Transformation)" in ETL.  We are currently ignoring the "L (Load)" in ETL.

**Source:**  "sample_analytics".  To know more about the source please visit the page: https://www.mongodb.com/docs/atlas/sample-data/sample-analytics/

**Tools:**   MongoDB Shell.

**Business Logic:**

**1.	accounts:**

    a.	For the products with "CurrencyService" increase the limit to 5%
		
**2.	customers:**

    a.	The customer name should be displayed in the template - <Lastname>(.)<space><Firstname>.  Here the lastname should be capitalized.
    b.	The domain of the customer’s email address should be changed from “@hotmail.com” to “@gmail.com”.
    c.	Records of customers with tiers “Gold” and “Platinum” should only be processed.
		
**3.	transactions:**

    a.	Transactions performed for the period from 2010 to 2015 should only be considered.
    b.	Correct the transaction_count field in each document after performing the above filter (filtering based on time period).
    c.	Limit the decimals of Price and Total fields to two places.
