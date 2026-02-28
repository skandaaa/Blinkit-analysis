# Blinkit-data-analysis
"I created an interactive Power BI dashboard for Blinkit’s data, focusing on making it simple, clear, and visually engaging. The dashboard turned complex raw data into easy-to-read visuals, helping stakeholders quickly spot trends, track key metrics, and make smarter business decisions."

Data Storytelling with Power BI: Blinkit Case Study :

1.Collect & prepare the data

Pull data from Excel/CSV/SQL into Power Query. Clean: rename columns, set data types, remove duplicates, fill/mask nulls, unpivot where needed. Create a proper Date table.

2.Model the data

Create a star-schema (FactSales + dimension tables: Items, Outlets, Dates). Define relationships (1:*). Mark the Date table as the date table.

3.Create key measures (DAX)

Build concise measures used for KPI cards and visuals. Example DAX:
Total Sales = SUM(FactSales[SalesAmount])
Avg Sales = AVERAGE(FactSales[SalesAmount])
No of Items = DISTINCTCOUNT(FactSales[ItemID])
Avg Rating = AVERAGE(Outlets[Rating])
Fat Sales (LowFat) = CALCULATE([Total Sales], Items[FatContent] = "Low Fat")

4.Design visuals & layout

Add KPI cards (Total Sales, Avg Sales, No of Items, Avg Rating) at the top-left.

Use a left-side filter/slicer panel (Outlet Type, Outlet Size, Item Type).

Main area: line chart for outlet establishment trend, donut/pie for outlet size, horizontal bar for item-type sales, stacked bars for fat by outlet, and a matrix/table with conditional formatting for outlet type metrics (as in your image).

5.Styling & storytelling

Apply a consistent theme (Blinkit yellow + complementary greens), align visuals to a grid, use white space and subtle borders, add data labels and small annotations on key points. Use bookmarks to present different story slides (e.g., Overview → Deep Dive → Recommendations).

6.Add interactivity & UX

Enable cross-filtering between visuals, sync relevant slicers across pages, add drill-through pages and custom tooltips, and configure visual-level/page-level/report-level filters as needed. Design a mobile view if needed.

7.Optimize, test & publish

Optimize model (remove unused columns, disable “auto date/time” if needed), test filters and edge cases, verify numbers vs source. Publish to Power BI Service, set up scheduled refresh and row-level security or share links/dashboards with stakeholders.

8.Screenshot:
https://github.com/shvetz45/Blinkit-data-analysis/blob/main/blinkit%20data%20analysis%20dashboard.png
