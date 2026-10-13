Helpdesk Performance & SLA Analytics



A data analytics portfolio project by Divya Tadi


I worked on this project to practise how Python, SQL Server, and Power BI can be used together to analyse IT helpdesk tickets. I explored ticket volume, SLA breaches, resolution time, agent workload, and department-wise demand using a simulated dataset.

Dataset note: The data is simulated for learning and portfolio practice. The findings do not represent a real company.

____________________________________________________________________________________________________________________________________________________________________________________________

What I Worked On

- Reviewed and modified the Python dataset-generation script so its CSV output path works with my local project folders.
- Generated and checked CSV files for tickets, agents, departments, and SLA policies.
- Used SQL Server and SSMS to work with the helpdesk tables and explore ticket and SLA metrics.
- Worked with the Power BI report and reviewed its three report pages.
- Updated the project documentation and organised the project files for GitHub.
____________________________________________________________________________________________________

This repository builds on an existing project structure that I adapted for learning. I am documenting the work I personally performed rather than claiming that every part was created from scratch.

____________________________________________________________________________________________________________________________________________________________________________________________
Project Goal

The goal is to understand questions such as:
- How many helpdesk tickets are recorded?
- What percentage of eligible tickets breach their SLA?
- How long do tickets take to resolve?
- How many tickets remain open or in progress?
- How does ticket workload vary by agent and department?
- Which ticket categories or time periods may need further investigation?
___________________________________________________________________________________________________________________________________________________________________________________________

Tools Used

| Tool | How it is used in this project |
|---|---|
| Python | Generate the simulated dataset |
| Pandas and NumPy | Prepare and export tabular data |
| SQL Server and SSMS | Store, query, and analyse helpdesk data |
| Power BI | Explore metrics through report visuals |
| DAX | Calculate dashboard measures |
| Git and GitHub | Track and share project files |                                              Track and share project files
____________________________________________________________________________________________________________________________________________________________________________________________


Dataset
The project uses simulated data across four main tables:


| Table | Approximate row count | Purpose |
|---|---:|---|
| `tickets` | 8,000 | Ticket details, status, category, priority, and dates |
| `agents` | 20 | Support agent information |
| `departments` | 8 | Department information |
| `sla_policy` | 20 | SLA thresholds by category and priority |



The generated CSV files are stored in generated_data/ in my local project setup. Folder names can differ between versions of the project.

_____________________________________________________________________________________________________________________________________________________________________________________________
Project Structure

```text
Helpdesk-Performance-SLA-Analytics/
├── Data/
├── generated_data/
├── Python/
│   └── generate_dataset.py
├── SQL/
│   └── helpdesk_complete.sql
├── PowerBI/
│   └── Helpdesk_Performance_SLA_Analytics.pbix
├── Screenshots/
│   ├── Executive Overview.png
│   ├── SLA & Resolution Deep Dive.png
│   └── Agent & Department Performance.png
└── README.md
```

____________________________________________________________________________________________________________________________________________________________________________________________
Power BI Report

The report contains three pages:

1. Executive Overview


A summary of key helpdesk metrics, including total tickets, SLA breach rate, average resolution time, open backlog, first-call resolution (FCR), and critical tickets.

![Executive Overview](Screenshots/Executive%20Overview.png)

____________________________________________________________________________________________________________________________________________________________________________________________

2. SLA & Resolution Deep Dive


A closer look at SLA performance and resolution time across categories and other ticket dimensions.

![SLA & Resolution Deep Dive](Screenshots/SLA%20%26%20Resolution%20Deep%20Dive.png)

_____________________________________________________________________________________________________________________________________________________________________________________________


3. Agent & Department Performance


A comparison of ticket workload across agents and departments.

![Agent & Department Performance](Screenshots/Agent%20%26%20Department%20Performance.png)

_____________________________________________________________________________________________________________________________________________________________________________________________


Dashboard Metrics

The report previously displayed the following headline values. These values can change after data regeneration, refreshes, or filter changes, so they should be rechecked in Power BI before being presented as final results.

| Metric | Displayed value |
|---|---:|
| Total Tickets | 8,000 |
| SLA Breach Rate | 23.49% |
| Average Resolution Time | 29.3 hours |
| Open Backlog | 1,177 |
| First-Call Resolution (FCR) | 95.34% |
| Critical Tickets | 603 |

_____________________________________________________________________________________________________________________________________________________________________________________________
How to Run the Project

1. Install Python packages


Open a terminal in the project root and run:


py -m pip install pandas numpy Faker

2. Generate the CSV files


Run:


py Python/generate_dataset.py


Check the script's output path and confirm the CSV files were created in the expected folder. Running the script again may replace existing generated CSV files, so keep a backup if you need the current data.

_____________________________________________________________________________________________________________________________________________________________________________________________

3. Set up SQL Server

1. Open SQL Server Management Studio (SSMS) and connect to your local SQL Server instance.
2. Create or select the HelpdeskAnalytics database.
3. Import the CSV files into the matching tables, checking the column names and data types.
4. Open SQL/helpdesk_complete.sql and run it section by section after reviewing which tables or views already exist. Avoid blindly rerunning database-creation statements.

_____________________________________________________________________________________________________________________________________________________________________________________________

4. Open Power BI

1. Open PowerBI/Helpdesk_Performance_SLA_Analytics.pbix.
2. If prompted, update the data source to your local SQL Server instance.
3. Refresh the report.
4. Check that the visuals and KPI values match the data and measure definitions.
_____________________________________________________________________________________________________________________________________________________________________________________________

What I Learned

- How a Python script can generate data for analysis.
- How related tables can be organised and queried in SQL Server.
- Why data types, missing values, duplicate IDs, and date logic need to be checked.
- How SLA measures can be used to study support performance.
- How a multi-page Power BI report can present operational metrics.
- Why KPI definitions and filters must be checked before interpreting results.
_____________________________________________________________________________________________________________________________________________________________________________________________

Next Improvements

- Add screenshots and explanations of the SQL queries I personally tested.
- Document the exact DAX measures and verify each KPI definition.
- Validate the report after refreshing it from my local SQL Server.
- Add a short section explaining the changes I made to the original project files.
____________________________________________________________________________________________________________________________________________________________________________________________
About

Author: Divya Tadi



Project: Helpdesk Performance & SLA Analytics



Tools: Python, Pandas, NumPy, SQL Server, SSMS, Power BI, DAX, GitHub


Domain: IT Helpdesk Analytics and SLA Monitoring


_____________________________________________________________________________________________________________________________________________________________________________________________

Acknowledgement

This project was adapted for learning and portfolio purposes. I made changes to the Python dataset-generation script, worked with the SQL Server database, and explored the Power BI dashboard to improve my data analytics skills.

The project helped me gain practical experience with Python, SQL Server, and Power BI.
