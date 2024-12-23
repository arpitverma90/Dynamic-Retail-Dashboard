# Dynamic Retail Dashboard in Excel
### Overview

The **Dynamic Retail Dashboard** is an interactive tool designed in Excel to visualize and analyze retail data. It connects to datasets hosted on GitHub, utilizes Power Query for data transformation, and presents insights through dynamic charts and Key Performance Indicators (KPIs). This dashboard addresses critical business challenges, helping businesses make data-driven decisions.

---

### **Datasets Used**

1. **Orders Table**
   - This table includes detailed information about customer orders, including product details, shipping, and financial metrics.

   **Sample Data**:
   | Order ID          | Returned | Order Date | Ship Date | Ship Mode   | Customer Name  | Segment    | Country       | Market | Sales   | Profit  | Discount |
   |-------------------|----------|------------|-----------|-------------|----------------|------------|---------------|--------|---------|---------|----------|
   | CA-2012-124891    | No       | 31-07-2020 | 31-07-2020 | Same Day    | Rick Hansen    | Consumer   | United States | US     | 2309.65 | 762.18  | 0        |
   | IN-2013-77878     | Yes      | 05-02-2021 | 07-02-2021 | Second Class | Justin Ritter  | Corporate  | Australia     | APAC   | 3709.40 | -288.77 | 0.1      |
   | IN-2013-71249     | No       | 17-10-2021 | 18-10-2021 | First Class | Craig Reiter   | Consumer   | Australia     | APAC   | 5175.17 | 919.97  | 0.1      |

2. **Returns Table**
   - Tracks the orders that have been returned, with the market details for each return.

   **Sample Data**:
   | Returned | Order ID           | Market   |
   |----------|--------------------|----------|
   | Yes      | MX-2013-168137     | LATAM    |
   | Yes      | US-2011-165316     | LATAM    |
   | Yes      | ES-2013-1525878    | EU       |
   | Yes      | CA-2013-118311     | United States |

3. **People Table**
   - Contains information about sales representatives and the regions they cover.

   **Sample Data**:
   | Person            | Region   |
   |-------------------|----------|
   | Anna Andreadi     | Central  |
   | Chuck Magee       | South    |
   | Kelly Williams    | East     |
   | Matt Collister    | West     |
   | Deborah Brumfield | Africa   |

---

### **Problem Statements Solved with Steps**

#### 1. **Key Performance Indicators (KPIs)**
   - **Objective**: Dynamically display key metrics such as Total Sales, Total Profit, Total Quantity, Number of Orders, and Profit Margin.
   
   **Steps**:
   - Import the **Orders Table** using **Power Query**.
   - Create calculated columns for:
     - **Profit Margin**: `Profit / Sales`.
     - **Total Orders**: `Count of Order ID`.
   - Use Excel formulas to calculate:
     - **Total Sales**: `=SUM(Sales)`.
     - **Total Profit**: `=SUM(Profit)`.
     - **Total Quantity**: `=SUM(Quantity)`.
     - ![image](https://github.com/user-attachments/assets/0bcc10ed-26c1-4a80-bf07-68340ba76885)


   - Create a dynamic KPI table with visual elements like symbols (e.g., 💰 for Total Sales).
   - Here is the KPI table you requested in a simple table format:

| **Name**           | **Metric**             | **Symbol** |
|--------------------|------------------------|------------|
| **Total Sales**     | Sum of Sales           | 💰         |
| **Total Profit**    | Sum of Profit          | 📈         |
| **Total Quantity**  | Sum of Quantity        | 📦         |
| **No. of Orders**   | Count of Order ID      | 🛒         |
| **Profitability**   | Sum of Profitability   | 💹         |

---

#### 2. **Sales and Profit Analysis**
   - **Objective**: Track and visualize sales and profit trends over time.
   
   **Steps**:
   - Create a **Pivot Table** with `Order Date` grouped by Year and Month.
   - Add **Sales** and **Profit** as values.
   - Create a **Line Chart** to display trends.
   - Apply **Slicers** to filter data dynamically by category, market, or region.
   - ![image](https://github.com/user-attachments/assets/de0e58f1-a8b9-4121-bd2f-1e5941f153a9)



---

#### 3. **Category-Wise Profit**
   - **Objective**: Evaluate profit across different product categories.
   
   **Steps**:
   - Create a **Pivot Table** using `Category` as rows and `Profit` as values.
   - Sort the table in descending order of Profit.
   - Create a **Bar Chart** to display the category-wise profit.
   - Use **Slicers** for interactive filtering by region or year.
   - ![image](https://github.com/user-attachments/assets/02c9c20d-7886-4d6f-8da7-d82ab1a8f293)


---

#### 4. **Segment-Wise Sales Share (%)**
   - **Objective**: Visualize the sales share for each customer segment.
   
   **Steps**:
   - Create a **Pivot Table** with `Segment` as rows and `Sales` as values.
   - Calculate **Percentage Share**: `=Sales / Total Sales * 100`.
   - Use a **Pie** or **Donut Chart** to present the share visually.
   - Add **Labels** to show percentage values dynamically.
   - ![image](https://github.com/user-attachments/assets/45c7c8f7-07e7-4628-8301-f7c53b41e6d9)



---

#### 5. **Sales by Country**
   - **Objective**: Examine sales performance by country.
   
   **Steps**:
   - Create a **Pivot Table** with `Country` as rows and `Sales` as values.
   - Sort the table in descending order of Sales.
   - Use **Conditional Formatting** or a **Heatmap** to highlight top-performing countries.
   - Alternatively, use a **Geographic Map Chart** to visualize sales geographically.
   - ![image](https://github.com/user-attachments/assets/1c338170-af2a-4b09-b35b-89848f5cd381)


---

#### 6. **Top 5 Subcategories**
   - **Objective**: Identify the top 5 performing subcategories based on sales.
   
   **Steps**:
   - Create a **Pivot Table** with `Sub-Category` as rows and `Sales` as values.
   - Sort the table in descending order of Sales.
   - Filter the data to display only the **Top 5 Subcategories**.
   - Create a **Column Chart** to visualize the results.
   - ![image](https://github.com/user-attachments/assets/202369c5-9c2b-4974-a4be-e3584c49e4e2)


---

#### 7. **Bottom 5 Subcategories**
   - **Objective**: Highlight the bottom 5 subcategories with the lowest sales performance.
   
   **Steps**:
   - Use the same **Pivot Table** but sort it in ascending order of Sales.
   - Filter the data to display only the **Bottom 5 Subcategories**.
   - Create a **Column Chart** with contrasting colors to emphasize low-performing subcategories.
   - ![image](https://github.com/user-attachments/assets/deb29c4b-54cf-438c-98cf-41ce963ffb9c)




---

#### 8. **Yearly Sales Trends**
   - **Objective**: Analyze the trends in sales over the years.
   
   **Steps**:
   - Create a **Pivot Table** with `Order Date` grouped by Year.
   - Add **Sales** as values.
   - Create a **Line Chart** to show yearly trends.
   - Use **Slicers** to filter the data by category, region, or segment.
   - ![image](https://github.com/user-attachments/assets/10948cb4-7c3d-47a8-b15c-2a5e8785f6f3)


---

### **Dynamic Features**

The dashboard features several dynamic elements:
   - **Dynamic Charts**: Automatically update based on slicer selections.
   - **Power Query Integration**: Automates the process of data cleaning and transformation.
   - **KPI Table**: Provides a quick summary of critical business metrics.

---

### **Next Steps for Extension**

Further improvements that can be added to the dashboard include:
   - **Return Analysis**: Analyze return rates by market or product category.
   - **Top and Bottom Customers**: Identify the most and least profitable customers.
   - **Market Analysis**: Compare sales performance across various markets.
   - **Product Analysis**: Evaluate the performance of individual products.

---

### **Significance**

The **Dynamic Retail Dashboard** helps businesses:
   - Monitor key metrics through KPIs.
   - Gain insights into trends by category, segment, and geography.
   - Make strategic decisions to improve business performance.

---

### **Visuals**

The repository includes:
   - Visual representations for each solved problem.
   - Screenshots of the final dashboard with all components in action.
   - ![image](https://github.com/user-attachments/assets/6da4b9dc-4397-4831-beec-eb15f856a2b3)


---

