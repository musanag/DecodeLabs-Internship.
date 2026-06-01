# Data Analytics Project — Data Cleaning

## Overview
This project performs data cleaning and preprocessing on a sales/orders dataset using Python and pandas, preparing it for downstream analysis.

## Files
| File | Description |
|------|-------------|
| `Project1.ipynb` | Jupyter notebook containing all data cleaning steps |
| `Dataset for Data Analytics.xlsx` | Raw input dataset |
| `Clean Dataset for Data Analytics.xlsx` | Cleaned output dataset |

## Dataset
The dataset contains e-commerce order records with the following columns:

| Column | Type | Description |
|--------|------|-------------|
| `OrderID` | string | Unique order identifier |
| `Date` | datetime | Order date |
| `CustomerID` | string | Unique customer identifier |
| `Product` | string | Product name (e.g. Monitor, Phone, Tablet) |
| `Quantity` | int | Number of units ordered |
| `UnitPrice` | float | Price per unit |
| `ShippingAddress` | string | Delivery address |
| `PaymentMethod` | string | Payment method used |
| `OrderStatus` | string | Current order status (Shipped, Delivered, Cancelled, Returned) |
| `TrackingNumber` | string | Shipment tracking number |
| `ItemsInCart` | int | Total items in customer's cart |
| `CouponCode` | string | Discount coupon applied (if any) |
| `ReferralSource` | string | Marketing channel (e.g. Instagram, Email, Facebook) |
| `TotalPrice` | float | Total order value |

## Data Cleaning Steps

1. **Load data** — Read the raw Excel file into a pandas DataFrame.
2. **Check for null values** — Found **309 missing values**, all located in the `CouponCode` column.
3. **Handle missing values** — Filled nulls in `CouponCode` with the string `'NaN'` to indicate no coupon was used.
4. **Check for duplicates** — No duplicate rows found.
5. **Validate data types** — Confirmed all columns have correct types (dates as `datetime64`, prices as `float64`, quantities as `int64`).
6. **Export cleaned data** — Saved the cleaned dataset to a new Excel file.

## Requirements
- Python 3.x
- pandas
- openpyxl

Install dependencies:
```bash
pip install pandas openpyxl
```

## Usage
Open and run `Project1.ipynb` in Jupyter Notebook or JupyterLab:
```bash
jupyter notebook Project1.ipynb
```
