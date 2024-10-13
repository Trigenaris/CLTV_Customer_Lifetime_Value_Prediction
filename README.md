# CLTV(Customer Lifetime Value) Prediction

## Business Problem

In this section, we are going to apply **cltv prediction** on a specific [retail dataset](https://www.kaggle.com/code/trigenaris/cltv-customer-lifetime-value-prediction/input) and then **functionalize** the whole process.

In the end, the whole process will be functionalized, and a CSV or Excel file will be created if the user requests it.

The calculations and processes are shown below respectively:

* Importing required libraries:
    * numpy
    * pandas
    * datetime
    * matplotlib
    * sklearn
    * lifetimes (needs installation if not used before)
* Specific settings for pandas
* Importing and checking the dataset
* General information about the dataset
* Data Preprocessing:
    * Handling missing values
    * Removing the refunded items from the dataset
    * Correction of *Quantity* and *Price* columns
    * Calculation of *total price*
    * Creating a virtual current date
* Preparation of Lifetime Data Structure
    * Recency
    * T (Age of the customer)
    * Frequency
    * Monetary
* Setting BG-NBD Model
* Setting Gamma-Gamma Model
* Calculating cltv with BG-NBD Model and Gamma-Gamma Model
* Creation of Segments
* Exporting All Results to CSV File
* Functionalization of the Whole Process

______

## Dataset Story

[Dataset Link](https://www.kaggle.com/code/trigenaris/cltv-customer-lifetime-value-prediction/input)

**Context**

This Online Retail II data set contains all the transactions occurring for a UK-based and registered, non-store online retail between 01/12/2009 and 09/12/2011.The company mainly sells unique all-occasion gift-ware. Many customers of the company are wholesalers.

**Content**

Attribute Information:

* **InvoiceNo:** Invoice number. Nominal. A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation.
* **StockCode:** Product (item) code. Nominal. A 5-digit integral number uniquely assigned to each distinct product.
* **Description:** Product (item) name. Nominal.
* **Quantity:** The quantities of each product (item) per transaction. Numeric.
* **InvoiceDate:** Invice date and time. Numeric. The day and time when a transaction was generated.
* **UnitPrice:** Unit price. Numeric. Product price per unit in sterling (Â£).
* **CustomerID:** Customer number. Nominal. A 5-digit integral number uniquely assigned to each customer.
* **Country:** Country name. Nominal. The name of the country where a customer resides.
