# StockSense — Inventory Risk Intelligence

A Power BI inventory analytics project designed to monitor stock levels, identify stockout risks, and evaluate supplier performance.

## Project Overview

StockSense helps inventory teams answer practical operational questions:

- Which products need to be reordered?
- Which SKUs are at risk of stockout?
- How much inventory value is currently held?
- Which suppliers have longer lead times or lower on-time delivery rates?
- How can inventory and supplier performance be monitored in one dashboard?

## Tools & Technologies

- **Power BI Desktop** — interactive dashboard and data visualization
- **DAX** — KPI measures and inventory risk classification
- **CSV / relational data modeling** — product, supplier, inventory, and purchase-order data

## Dataset

The project uses four related datasets:

| Dataset | Purpose |
|---|---|
| `Products.csv` | Product categories, costs, reorder points, and target demand |
| `Suppliers.csv` | Supplier regions, lead times, delivery rates, and defect rates |
| `InventoryDaily.csv` | Daily demand, sales, stock balances, and inventory value |
| `PurchaseOrders.csv` | Order quantities, delivery dates, and late-delivery indicators |

**Data note:** The dataset is simulated for portfolio and learning purposes. It does not represent actual company operations.

## Dashboard Features

- Current stock units and inventory value
- SKUs below their reorder points
- Stockout SKU monitoring
- Product-level inventory risk classification
- Category-level stock comparison
- Supplier on-time delivery performance
- Average supplier lead-time comparison
- Category and supplier slicers for interactive exploration

## Key Performance Indicators

The dashboard includes four primary KPIs:

1. **Current Stock Units** — total closing stock at the latest available inventory date.
2. **Current Inventory Value** — inventory value at the latest available date.
3. **SKUs Below Reorder Point** — number of products at or below their reorder thresholds.
4. **Stockout SKUs** — number of products with zero or negative current stock.

## Inventory Risk Logic

Products are classified using their latest stock balance and configured reorder point:

- **Critical - Stockout:** Current stock is zero or less.
- **Reorder Now:** Current stock is positive but at or below the reorder point.
- **Healthy:** Current stock is above the reorder point.
- **Unknown:** A reliable current stock value is unavailable.

## Data Model

The Power BI model connects products to inventory history and purchase orders using SKU. Supplier information is connected to products using SupplierID.

This structure supports product-level inventory analysis and supplier-level performance reporting.

## How to Use

1. Download or clone this repository.
2. Open `StockSense_Inventory_Risk_Intelligence.pbix` in Power BI Desktop.
3. If prompted, update the CSV source paths to the location of the downloaded dataset.
4. Refresh the data if necessary.
5. Use the category and supplier slicers to explore the dashboard.

## Project Structure

```text
StockSense-Inventory-Risk-Intelligence/
├── README.md
├── StockSense_Inventory_Risk_Intelligence.pbix
├── data/
│   ├── Products.csv
│   ├── Suppliers.csv
│   ├── InventoryDaily.csv
│   └── PurchaseOrders.csv
└── screenshots/
    └── dashboard.png
```

The screenshot is optional until you add it. Keep the repository structure aligned with the files you actually upload.

## Learning Outcomes

- Building a relational data model in Power BI
- Writing DAX measures for inventory KPIs
- Creating business-oriented inventory risk rules
- Visualizing supplier delivery and lead-time performance
- Designing interactive dashboards for operational decision-making

## Future Improvements

- Add demand forecasting and projected stockout dates.
- Incorporate supplier risk scoring.
- Compare inventory holding costs against service levels.
- Add date-based trend analysis and replenishment recommendations.

---

**Project:** StockSense — Inventory Risk Intelligence  
**Purpose:** Data analytics portfolio project  
**Dataset:** Simulated data for educational use
