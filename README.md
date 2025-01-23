# B2B-Courier-Charges-Accuracy-Analysis-using-Python

In the fast-paced e-commerce industry, efficient and accurate billing is crucial for seamless order fulfillment. This project focuses on **B2B Courier Charges Accuracy Analysis**, where the goal is to assess and verify the accuracy of fees charged by courier companies for shipping goods in B2B transactions.

---

## 📋 Problem Statement

Courier companies often generate invoices that may not align with a company's own estimates, leading to discrepancies in charges. These inaccuracies can arise due to:
- Incorrect weight slabs.
- Mismatched delivery zones.
- Additional or overlooked charges.

This project aims to analyze these discrepancies and ensure companies are billed correctly.

---

## 🚀 Objective

The goal of this project is to:
- Identify discrepancies between expected and actual courier charges.
- Quantify the extent of overcharging and undercharging.
- Provide a clear summary of charge accuracy through data visualization.

---

## 🛠️ Methodology

1. **Data Cleaning**:
   - Removed unnecessary columns from datasets (e.g., unnamed columns).
   - Checked and handled missing values.

2. **Data Merging**:
   - Merged multiple datasets: `Order Report`, `SKU Master`, `Pincode Mapping`, `Courier Invoice`, and `Courier Company Rates`.

3. **Feature Engineering**:
   - Calculated `Weight Slabs` for shipments.
   - Determined `Expected Charges` based on company-defined rates.

4. **Analysis**:
   - Compared expected charges to billed charges.
   - Categorized orders as correctly charged, overcharged, or undercharged.
   - Summarized the results in a DataFrame.

5. **Visualization**:
   - Created a pie chart to depict the proportion of correctly charged, overcharged, and undercharged orders.

---

## 📊 Key Findings

| Description                                      | Count | Amount (Rs.) |
|--------------------------------------------------|-------|--------------|
| Total Orders where ABC has been correctly charged | 12    | 507.6        |
| Total Orders where ABC has been overcharged      | 382   | 33,750.5     |
| Total Orders where ABC has been undercharged     | 7     | -165.2       |

---

## 📁 Datasets Used

1. **Order Report**:
   - Contains order details like `Order ID` and `SKU`.

2. **SKU Master**:
   - Maps SKUs to their respective weights.

3. **Pincode Mapping**:
   - Links `Warehouse Pincode` to `Customer Pincode` and `Delivery Zone`.

4. **Courier Invoice**:
   - Contains billed charges, shipment types, and zones.

5. **Courier Company Rates**:
   - Defines rate slabs for various delivery zones.

---

## 🧩 Features Implemented

- **Weight Slab Calculation**:
  - Calculated the correct weight slab (0.5 KG increments).
- **Expected Charges**:
  - Used company-defined rates to calculate expected costs.
- **Discrepancy Analysis**:
  - Highlighted differences between expected and billed charges.
- **Visualization**:
  - Used Plotly to create an interactive pie chart of charge accuracy.

---

## 📊 Data Visualization

The following chart represents the proportion of orders that were:
- Correctly charged.
- Overcharged.
- Undercharged.

### Pie Chart Example:
```python
import plotly.graph_objects as go

fig = go.Figure(data=[go.Pie(
    labels=["Correctly Charged", "Overcharged", "Undercharged"],
    values=[12, 382, 7],
    textinfo='label+percent',
    hole=0.4
)])

fig.update_layout(title='Proportion of Charge Accuracy')
fig.show()

## 💻 Tools and Technologies

- **Python Libraries**:
  - Pandas: Data manipulation and analysis.
  - Plotly: Interactive visualizations.
  - NumPy: Mathematical computations.

## Acknowledgements
Special thanks to Aman Kharwal for the original inspiration and guidance in solving real-world data problems.