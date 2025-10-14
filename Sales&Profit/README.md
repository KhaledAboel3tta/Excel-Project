
---

# 📊 Sales & Profit Dashboard (Microsoft Excel)

This project features a comprehensive and interactive **Sales & Profit Dashboard** meticulously designed and built entirely within Microsoft Excel. The dashboard transforms raw transactional data into clear, actionable business insights, focusing on sales performance, profitability trends, and customer segmentation.

##  Project Overview and Key Features

The primary goal of this dashboard is to provide a visually clear and polished analytical tool.

At the top of the dashboard, users can immediately view the **Key Metrics** showing **Total Sales** and **Total Profit**. The entire dashboard is designed to update automatically as the underlying data changes, facilitated by linking key metrics directly to Pivot Table values using the equals sign (`=`).

### Core Visualizations Included:

| Visualization | Analytical Focus | Chart Type | Source |
| :--- | :--- | :--- | :--- |
| Key Metrics | Total Sales & Total Profit | Text Boxes/Icons | |
| Profit by Year | Annual Profit Distribution | Column Chart | |
| Sales by Category | Detailed Sales Breakdown by Subcategory | Funnel Chart | |
| Customer Count by Year | Unique Customer Acquisition Trends | Donut Chart | |
| Sales by State | Geographical Sales Performance | Map Chart | |
| Monthly Sales Trends | Sales performance over time | Column Chart | |
| Top Five Customers Profit | Identification of most profitable customers | Bar Chart | |

---

##  Implementation & Technical Effort

The project required extensive data preparation, sophisticated Pivot Table techniques, and detailed UI/UX design to achieve a professional look.

### 1. Data Preparation and Structure

*   The initial step involved preparing the data by selecting the entire dataset and applying formatting for visual clarity.
*   Filters were applied via the Data tab, and a chosen table design was selected for a polished look.
*   The table view was enhanced using **Freeze Panes** (specifically "freeze top row").
*   The workbook structure utilizes two new sheets: one dedicated to **Pivot Tables** and one for the **Dashboard** visualization.
*   Grid lines were unchecked under the View tab on both the Pivot Table sheet and the Dashboard sheet to ensure a clean visual display.

### 2. Advanced Analytical Effort (Pivot Tables)

Various Pivot Tables were created by selecting the entire dataset and positioning them in the dedicated Pivot Table sheet. Key analytical techniques utilized include:

*   **Metric Calculation:** Calculating the sum of sales and sum of profit by dragging respective fields into the Values section.
*   **Sales by Subcategory:** The data was organized by dragging the Subcategory field to the Row section and Sales to the Value section. Results were sorted from **"largest to smallest"**.
*   **Dynamic Data Linking:** To ensure automatic updates for subcategory sales, a dynamic table was created on the side using the **`GETPIVOTDATA`** function, linking cells back to the pivot cell references.
*   **Unique Customer Count:** To accurately count unique customers by year, the Customer Name and Year columns were copied, pasted, and processed using the **Remove Duplicates** function before creating the necessary Pivot Table.
*   **Top 5 Filtering:** For the **Top Five Customers Profit** analysis, the **Value Filters** option was utilized within the Pivot Table settings to specifically select "Top 5" (changing the default "Top 10") and sorting the results from largest to smallest.
*   Formatting (dollar signs, decreased decimal values, and alignment) was consistently applied across all Pivot Tables for a professional appearance.

### 3. Dashboard Design and Visualization

The dashboard layout was constructed using the **Rectangle Rounded Corner shape**. Design features include:

*   **Visual Effects:** Applying a **Shadow effect** and utilizing **Gradient Fill** in the Format Pane to define the section colors.
*   **Chart Formatting:** All charts were formatted with **no shape fill** and **no shape outline** for a clean aesthetic. All field buttons on the charts were hidden.
*   **Chart Specifics:**
    *   The **Profit by Year** Column Chart had its data series overlap set to 0% and gap width set to 150%.
    *   The **Customer Count by Year** Donut Chart had its hole size specifically set to 50%.
    *   The **Sales by State** visualization utilized the specialized **Map Chart** functionality.

### 4. Interactivity (Slicers and Connections)

Interactivity is achieved through the use of Slicers for filtering data by **Year, Category, or Month**.

*   **Customization:** Slicers were visually customized (e.g., using custom color code `0C769E` for fill, Calibri font, and dark teal borders) to seamlessly match the overall dashboard design.
*   **Seamless Integration:** The critical step involved linking the slicers to the dashboard: by right-clicking each slicer and selecting **"Report Connections,"** they were explicitly linked to **all the Pivot Tables** on the dashboard, ensuring they filter the data consistently across all visualizations.
*   A refresh icon was also included to refresh all data when clicked.

---

## 💻 Requirements

*   Microsoft Excel (A modern version supporting features like Map Chart is recommended).

---

*Explore the Excel file to examine the data modeling and professional design techniques used in this project.*
