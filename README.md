Description:
This Power BI dashboard provides a comprehensive analysis of item pricing (MRP), category performance, and outlet trends. It helps stakeholders understand which product types and outlets contribute the most to pricing and sales patterns, with insights broken down by fat content, outlet types, and item categories.

 Key Features:
KPI Cards
Total MRP: Displays the average MRP across all items.

Regular Count: Total count of items labeled with "Regular" fat content.

Low Fat Count: Total count of items labeled with "Low Fat" fat content.

 Treemap: MRP by Outlet
Visualizes the sum of item MRP by outlet identifier to highlight top-performing stores.

 Stacked Column Chart: MRP by Outlet Type and Item Type
Compares item categories across different outlet types to show distribution and concentration of MRP.

 Bar Chart: Total MRP by Item Type
Highlights which item types contribute most to the overall MRP.

 Line Chart: Frequency Chart Distribution
Shows a line graph of total MRP across item types, sorted to visualize top and low performers.

 100% Stacked Column Chart: Fat Content in Outlet
Displays the proportion of item fat content (Low Fat, Regular) across outlet types using MRP as a weight

Dax Measures Used:
Average MRP = AVERAGE('Sheet1'[Item_MRP])
Total Items = DISTINCTCOUNT('Sheet1'[Item_Identifier])
Total Outlets = DISTINCTCOUNT('Sheet1'[Outlet_Identifier])
Total MRP = AVERAGE('Sheet1'[Item_MRP]) -- shown as KPI
Regular Count = CALCULATE(COUNTROWS('Sheet1'), 'Sheet1'[Item_Fat_Content] = "Regular")
Low Fat Count = CALCULATE(COUNTROWS('Sheet1'), 'Sheet1'[Item_Fat_Content] = "Low Fat")

Use Cases:
Identify high-value product categories.

Analyze item pricing distribution across different outlets.

Monitor how fat content affects MRP performance.

Support inventory, pricing, or marketing decisions.


