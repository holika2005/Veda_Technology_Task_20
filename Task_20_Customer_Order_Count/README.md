# Task 20 — Customer Order Count

## Objective
Count distinct orders per customer and identify frequent buyers using the provided Superstore dataset.

## Tool used
**Microsoft Excel only.** SQL was not used, so the task uses one of the tools listed in the task instructions.

## Dataset
`sample_superstore.xlsx`, `Raw_Data` sheet. The original rows are included in the analysis workbook's `Source Data` sheet for traceability.

## Deliverables
- `Task_20_Customer_Order_Count_Analysis.xlsx`
  - **Summary** — dataset and analysis overview.
  - **Customer Order Count** — all customers ranked by distinct order count, with order-line count and total sales/quantity where available.
  - **Top Customers** — top 20 frequent buyers.
  - **Source Data** — source rows used in the analysis.

## Method
1. Imported the Superstore `Raw_Data` sheet into Excel.
2. Excluded rows missing either `Order ID` or `Customer ID` from the customer count.
3. Grouped records by `Customer ID` and `Customer Name`.
4. Counted **distinct Order ID values** for each customer. This avoids counting the same order multiple times when it contains multiple product lines.
5. Sorted customers from highest to lowest distinct order count and extracted the top 20.

## Interview notes
- **Customer vs. order count:** a customer is a person/account; an order is a transaction. One customer can place multiple orders.
- **Why Customer ID matters:** it is a stable identifier for grouping purchases and reduces the risk of treating name variations as separate customers.

## Reproducibility note
The workbook contains calculated results based on the supplied dataset. If the source data changes, rerun the grouping/counting steps to refresh the result.
