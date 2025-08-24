<h1>Amazon Sales Report Analysis</h1>

This project analyzes Amazon Sales Data to uncover key insights such as sales trends, customer segments, and business performance (B2B vs B2C).
The analysis is performed using Python (pandas, matplotlib, seaborn).

<h1>Objectives</h1>

Understand sales distribution across different order statuses

Compare B2B vs B2C performance (both revenue and order count)

Identify sales trends and patterns for better decision making

<h1>Dataset</h1>

Columns include:

Status → Order status (Shipped, Cancelled, Pending, etc.)

B2B → Indicates if order is Business-to-Business (B2B) or Business-to-Customer (B2C)

Amount → Order amount (revenue per transaction)

(Dataset not included in repo due to confidentiality. Replace with your own dataset to replicate analysis.)

<h1>Key Analysis</h1>
<h2>1. Order Status Distribution</h2>
df['Status'].value_counts().plot(
    kind='pie', 
    autopct='%1.1f%%', 
    title='Order Status'
)


Shows percentage of orders by status (Shipped, Cancelled, etc.)

<h2>2. B2B vs B2C Revenue</h2>
df.groupby('B2B')['Amount'].sum().plot(
    kind='bar', 
    title='B2B vs B2C Sales (Revenue)'
)


Compares total revenue from B2B vs B2C customers

<h2>3. B2B vs B2C Sales Share (Order Count %)</h2>
b2b_sales_count = df['B2B'].value_counts()
b2b_sales_percent = (b2b_sales_count / b2b_sales_count.sum()) * 100

b2b_sales_percent.plot(
    kind='bar', 
    title='B2B vs B2C - % of Sales (Order Count)'
)


Shows the share of total orders that come from B2B vs B2C

<h1>Example Insights</h1>

Majority of orders are in Shipped status

While B2C orders are higher in count, B2B contributes significantly to revenue

This suggests B2B orders are larger in value per transaction

<h1>Tech Stack</h1>

Python 3.x

Pandas → Data cleaning & aggregation

Matplotlib / Seaborn → Data visualization

<h1>How to Run</h1>

Clone this repository:

git clone https://github.com/your-username/amazon-sales-analysis.git
cd amazon-sales-analysis

Install dependencies:

pip install pandas matplotlib seaborn

Run Jupyter Notebook or Python script:

jupyter notebook analysis.ipynb

<h1>Future Work</h1>
-Add time-series analysis of sales trends
-Perform customer segmentation
-Create interactive dashboard with Plotly or Power BI



<h2>✨ Built with curiosity for data-driven insights by Anvisha Trivedi</h2>

