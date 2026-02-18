# 📦 Delivery Performance Analysis — Group 4 | Section A

## Project Overview

This project analyzes courier delivery performance across major Indonesian cities using a structured dataset of e-commerce orders. The goal is to uncover insights about delivery efficiency, courier reliability, product satisfaction, and geographic performance — enabling data-driven decisions for logistics optimization.

The analysis covers **8,449 total orders** across **5 courier services** and **20 cities**, with an average delivery time of **2.81 days** and an average product rating of **3/5**.

---

## Repository Structure

```
📁 Root
├── 📁 RawDataset/          # Original, unmodified dataset
├── 📁 Cleaned/             # Cleaned and transformed dataset
├── 📁 Calculations_Pivots/ # Pivot tables and calculated metrics
├── 📁 Dashboard/           # Final dashboard file(s)
├── 📄 Documentation        # Project report / analysis write-up
├── 📄 Presentation         # Slide deck for viva
└── 📄 README.md            # This file
```

---

## Data Dictionary

| Column | Description |
|---|---|
| `product_id` | Unique identifier for each product/order |
| `order_date` | Date the order was placed (format: DD/MM/YY) |
| `courier_delivery` | Courier service used (J&T Express, Jne, Ninja Xpress, Pos Indonesia, Sicepat) |
| `city` | Destination city of delivery |
| `district` | Specific district within the city |
| `type_of_delivery` | Delivery tier: Express, Next Day, Reguler, Same Day |
| `estimated_delivery_time_days` | Estimated number of days for delivery |
| `product_rating` | Customer rating of the product (scale: 1–5) |

---

## Cleaning Notes

The following transformations were applied to prepare the dataset for analysis:

- **Removed** duplicate or irrelevant entries
- **Reformatted** `order_date` column to a consistent `YYYY-MM-DD` format (previously inconsistent)
- **Cleaned** `estimated_delivery_time_days`: removed letters, words, and missing/null values
- **Standardized** `courier_delivery` values to proper case (e.g., `jne` → `Jne`)
- **Standardized** `city` values to proper case
- **Standardized** `district` values to proper case
- All cleaning steps are documented in the `Cleaned/` folder with a change log

---

## Key Insights

### 🚚 Courier Performance
- All five couriers (J&T Express, Jne, Ninja Xpress, Pos Indonesia, Sicepat) perform very similarly, with average delivery times clustered tightly between **2.74 and 2.87 days**.
- **Ninja Xpress** has the fastest grand average delivery time (~2.73 days).
- **Pos Indonesia** has the slowest average (~2.87 days).
- Order share is nearly equal across all couriers (~19.6%–20.7%), indicating no single dominant player.

### 📅 Delivery Type
- **Express** deliveries are the fastest on average (~2.74 days).
- **Same Day** deliveries, counterintuitively, take the longest on average (~2.86 days) — possibly due to last-mile constraints or dataset definition.
- Delivery time differences across types are minimal, suggesting the dataset may reflect estimated rather than actual delivery times.

### ⭐ Product Ratings
- Average product ratings are consistent across all couriers, ranging from **~2.94 to 3.03**.
- **Pos Indonesia** has the highest average product rating (~3.03).
- **J&T Express** has the lowest (~2.99), but the difference is negligible.

### 🏙️ Top Cities for Fastest Delivery
- Cities with the fastest average delivery times include **Malang** (~2.61 days), **Surakarta** (~2.66 days), and **Pekanbaru** (~2.72 days).
- Cities with the slowest delivery times include **Depok** (~2.95 days), **Semarang** (~2.97 days), and **Bogor** (~2.93 days).

### 📊 Order Volume
- Total orders analyzed: **8,449**
- Breakdown by courier: J&T Express (1,653), Jne (1,671), Ninja Xpress (1,665), Pos Indonesia (1,715), Sicepat (1,745)

---

## Dashboard Summary

The interactive dashboard was built in **Google Sheets** and includes the following visualizations:

| Visual | Description |
|---|---|
| **KPI Cards** | Total Orders, Grand Avg Delivery Time, Avg Product Rating |
| **Bar Chart — Avg Delivery Time by Courier** | Horizontal bars comparing delivery speed across all 5 couriers |
| **Bar Chart — Pricept Time by Courier** | Delivery time breakdown by delivery type (Express, Next Day, Reguler, Same Day) |
| **Donut Chart — Order Share by Courier** | Proportional share of total orders per courier |
| **Bar Chart — Product Rating by Courier** | Average customer rating per courier |
| **Grouped Bar Chart — Delivery Stats by Type per Courier** | Cross-analysis of delivery type performance across couriers |
| **Bar Chart — Top Cities for Fastest Delivery** | Ranked city-level delivery time performance |
| **Slicers** | Filters for `courier_delivery`, `type_of_delivery`, and `city` |

> **Note:** Due to limitations in Google Sheets, slicers may render the dashboard as static when applied. This is a known platform constraint. The slicer logic is correctly structured to demonstrate filtering capability and will be discussed during the viva presentation.

---

## Tools Used

- **Microsoft Excel / Google Sheets** — Data cleaning, pivot tables, dashboard
- **Google Slides** — Presentation
- **GitHub** — Version control and project submission

---

## Team

**Group 4 — Section A**

> Submitted as per the project guidelines. Deadline: 18th February 2026 @ 11:59 PM IST.