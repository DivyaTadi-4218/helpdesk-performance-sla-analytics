Helpdesk Performance & SLA Analytics

An end-to-end data analytics project focused on analyzing IT helpdesk tickets, SLA compliance, ticket priorities, and support team performance using Python, SQL Server, and Power BI.

Project Overview

This project analyzes helpdesk ticket data to understand ticket volumes, resolution performance, SLA breaches, and open-ticket backlog. The goal is to turn raw ticket data into useful insights that can help support teams monitor performance and identify areas for improvement.

I worked with the existing project files, reviewed the dataset-generation logic, checked SQL queries against the database, and explored the Power BI dashboard and its key metrics.

Tools & Technologies

- Python: Dataset generation and CSV export using Pandas
- SQL Server: Data validation, aggregation, and SLA analysis
- Power BI: Interactive dashboard and KPI visualization
- Git & GitHub: Version control and project sharing

Dataset

The project includes these CSV files:

- "tickets.csv" — helpdesk ticket details
- "agents.csv" — support agent information
- "departments.csv" — department information
- "sla_policy.csv" — SLA targets by category and priority

The Python script exports the datasets to the "generated_data/" folder.

SQL Analysis

I used SQL queries to examine:

- Total ticket count and data quality
- Ticket distribution by status
- Ticket distribution by priority and category
- Response and resolution SLA breaches
- SLA breach percentages by priority

Power BI Dashboard

The dashboard presents key helpdesk metrics, including:

- Total tickets
- SLA breach percentage
- Average resolution time
- Open ticket backlog
- First Contact Resolution (FCR) rate
- Critical ticket count
- Ticket volume and SLA trends

The dashboard contains pages for executive overview, SLA and resolution analysis, and agent and department performance.

How to Run

1. Clone or download this repository.

2. Open the project folder in VS Code.

3. Install the required Python packages, if needed.

4. Run the dataset-generation script from the project root:
   
   "python Python/generate_dataset.py"

5. Open SQL Server Management Studio and execute the SQL scripts in the documented order.

6. Open the ".pbix" file in Power BI Desktop and configure the data source if required.

What I Learned

- Validating datasets and checking date fields
- Writing SQL queries for operational analysis
- Measuring SLA response and resolution breaches
- Understanding KPIs and presenting them in Power BI
- Organizing project files and documenting an analytics workflow

Project Attribution

This project is based on an existing project that I downloaded and modified. I am documenting the changes and analysis I worked on. Original source: [Add the original repository URL].

Author

[Tadi Divya]

GitHub: [Your GitHub profile URL]