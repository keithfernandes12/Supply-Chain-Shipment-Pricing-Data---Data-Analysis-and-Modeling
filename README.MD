# Supply Chain Shipment Pricing Data — Data Analysis and Modeling

## Overview

This project analyzes the **SCMS Delivery History Dataset**, which contains 10,324 records of supply chain shipments for health commodities (primarily ARV and HIV-related products) across multiple countries. The analysis explores shipment patterns, delivery performance, pricing, and manufacturing site activity.

**Dataset Source:** [Kaggle — Supply Chain Shipment Pricing Data](https://www.kaggle.com/divyeshardeshana/supply-chain-shipment-pricing-data)

## Dataset Description

The dataset contains 33 columns covering the full lifecycle of a shipment:

| Category | Columns |
|----------|---------|
| Identifiers | ID, Project Code, PQ #, PO/SO #, ASN/DN # |
| Logistics | Country, Managed By, Fulfill Via, Vendor INCO Term, Shipment Mode |
| Dates | PQ First Sent to Client Date, PO Sent to Vendor Date, Scheduled Delivery Date, Delivered to Client Date, Delivery Recorded Date |
| Product | Product Group, Sub Classification, Vendor, Item Description, Molecule/Test Type, Brand, Dosage, Dosage Form |
| Pricing | Unit of Measure (Per Pack), Line Item Quantity, Line Item Value, Pack Price, Unit Price |
| Shipping | Manufacturing Site, First Line Designation, Weight (Kilograms), Freight Cost (USD), Line Item Insurance (USD) |

## Analysis Summary

### 1. Country Distribution
- The dataset covers shipments to multiple countries, with the top recipients being concentrated in Sub-Saharan Africa and Southeast Asia.
- **Nigeria** leads in total pack price value at **25,620.72**.

### 2. Delivery Delay Analysis
- A `Delivery_Delay` feature was engineered by computing the difference between `Delivered to Client Date` and `Scheduled Delivery Date`.
- Country-level average delays were calculated to identify regions with persistent delivery issues.

### 3. Shipment Mode Breakdown
- **Air** is the dominant shipment mode, followed by Truck, Air Charter, and Ocean.
- Air shipments have a `Unit of Measure (Per Pack)` range of **1–1,000** with a mean of **82.35**.

### 4. Manufacturing Site Analysis
- **Aurobindo Unit III, India** is the most active manufacturing site overall (3,172 shipments) and for air shipments specifically (1,694).

### 5. First Line Designation
- The majority of shipments are classified as first-line designation products, meaning they don't require prior treatment with other drugs.

## Key Findings

- **Top country by total pack price:** Nigeria
- **Dominant shipment mode:** Air
- **Most active manufacturing site:** Aurobindo Unit III, India
- **Most active air manufacturing site:** Aurobindo Unit III, India

## Tech Stack

- **Python 3**
- **pandas** — data manipulation
- **NumPy** — numerical operations
- **Matplotlib / Seaborn** — static visualizations
- **Plotly** — interactive pie chart

## Project Structure

```
├── SCMS_Delivery_History_Dataset.csv          # Raw dataset
├── Supply_Chain_Shipment_Pricing_Data_-_Data_Analysis_and_Modeling.ipynb  # Analysis notebook
└── README.md                                  # This file
```

## How to Run

1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly
   ```
3. Open the notebook:
   ```bash
   jupyter notebook Supply_Chain_Shipment_Pricing_Data_-_Data_Analysis_and_Modeling.ipynb
   ```
