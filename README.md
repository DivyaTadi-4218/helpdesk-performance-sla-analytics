# Helpdesk Performance & SLA Analytics

**End-to-end IT support operations analytics using SQL Server, Power BI, and Python**

**Created by: Divya Tadi**

## Project Overview

This project analyses IT helpdesk ticket data to understand ticket volume, Service Level Agreement (SLA) compliance, resolution times, agent workload, and department-wise support demand. The goal is to help IT teams identify recurring bottlenecks and make data-informed staffing and process decisions.

> **Note:** This is a portfolio project using a generated/simulated helpdesk dataset. The findings describe this dataset and should not be interpreted as results from a real company.

## Business Problem

IT support teams handle hardware failures, software issues, access requests, and network problems. Without structured analysis, managers may struggle to identify:

- Which ticket categories and priorities have higher SLA breach rates
- Which agents may be overloaded
- How resolution time varies by ticket type
- When ticket demand is highest
- Which departments contribute most to ticket volume and backlog
- How reopened tickets affect support quality

## Project Objectives

- Store and analyse helpdesk data using SQL Server.
- Clean and validate imported data.
- Calculate response and resolution metrics against SLA policies.
- Build an interactive Power BI dashboard for operational insights.
- Use Python to generate and prepare the dataset.

## Tech Stack

| Tool | Purpose |
|---|---|
| Python, Pandas, NumPy | Dataset generation and data preparation |
| SQL Server | Data storage, cleaning, transformations, analytical queries and views |
| Power BI | Interactive dashboard and visual analysis |
| DAX | Measures and KPI calculations |
| GitHub | Project version control and documentation |

## Dataset

The project contains four main tables:

| Table | Records | Description |
|---|---:|---|
| `tickets` | 8,000 | Helpdesk tickets and their status, category, priority and dates |
| `agents` | 20 | Support agent details |
| `departments` | 8 | Requesting departments |
| `sla_policy` | 20 | SLA thresholds by category and priority |

The dataset is simulated for analytics practice. Ticket counts, SLA results, and other findings are specific to this dataset.

## Project Structure

```text
Helpdesk-Performance-SLA-Analytics/
├── Python/
│   └── generate_dataset.py
├── SQL/
│   └── helpdesk_complete.sql
├── PowerBI/
│   └── Helpdesk_Performance_SLA_Analytics.pbix
├── Screenshots/
│   ├── Executive Overview.png
│   ├── SLA & Resolution Deep Dive.png
│   ├── Agent & Department Performance.png
│   └── placeholder.txt
├── generated_data/
│   ├── tickets.csv
│   ├── agents.csv
│   ├── departments.csv
│   └── sla_policy.csv
└── README.md
```

*Folder and file names may vary slightly depending on the local project setup.*

## Power BI Dashboard

The Power BI report is organised into three analysis pages.

### 1. Executive Overview

Provides a high-level snapshot of helpdesk operations, including total tickets, SLA breach rate, average resolution time, open backlog, first-call resolution, and critical tickets.

![Executive Overview](Screenshots/Executive%20Overview.png)

### 2. SLA & Resolution Deep Dive

Explores SLA performance, resolution time by category, breach trends, and periods with higher ticket demand.

![SLA & Resolution Deep Dive](Screenshots/SLA%20%26%20Resolution%20Deep%20Dive.png)

### 3. Agent & Department Performance

Compares agent workloads and department-level ticket demand to help identify potential workload imbalances.

![Agent & Department Performance](Screenshots/Agent%20%26%20Department%20Performance.png)

## Key Dashboard Metrics

The current report displays the following headline metrics. Results can change when filters or data are refreshed.

| Metric | Displayed value |
|---|---:|
| Total Tickets | 8,000 |
| SLA Breach Rate | 23.49% |
| Average Resolution Time | 29.3 hours |
| Open Backlog | 1,177 |
| First-Call Resolution (FCR) | 95.34% |
| Critical Tickets | 603 |

## SQL Analysis

The SQL work covers:

- Creating and validating the core tables.
- Checking data types, null values, duplicate ticket IDs and date consistency.
- Calculating response and resolution durations.
- Comparing ticket performance with SLA thresholds by category and priority.
- Analysing ticket volume, SLA breaches, agent performance, department demand and time-based patterns.
- Preparing views for Power BI reporting.

**Important:** Run the SQL script section by section and review the database/table setup first. Do not rerun database-creation statements blindly if the database already exists.

## Python Workflow

The Python script in `Python/generate_dataset.py` generates the helpdesk dataset and exports CSV files. Review the script and output folder before rerunning it, because generating the dataset again may replace existing CSV outputs.

## How to Run the Project

### 1. Prepare the data

1. Install Python and the required packages used by the generator script.
2. Run `Python/generate_dataset.py` if you want to regenerate the simulated dataset.
3. Confirm the CSV files are available in the generated data folder.

### 2. Set up SQL Server

1. Open SQL Server Management Studio (SSMS) and connect to your SQL Server instance.
2. Create or select the `HelpdeskAnalytics` database.
3. Import the CSV files in this order: `departments`, `agents`, `sla_policy`, then `tickets`.
4. Review `SQL/helpdesk_complete.sql` and execute its sections in order, adapting any table or column definitions to match your imported schema.

### 3. Open Power BI

1. Open `PowerBI/Helpdesk_Performance_SLA_Analytics.pbix`.
2. If prompted, update the data source settings to point to your SQL Server instance.
3. Refresh the data and check that the report visuals load correctly.

## Key Takeaways

- SLA performance can be compared across ticket categories and priorities.
- Workload comparisons can help flag agents or departments that may need further investigation.
- Time-based analysis can help teams plan staffing around periods of higher demand.
- Dashboard metrics should always be interpreted with their definitions, filters, and SLA calculation rules in mind.

## About

**Author:** Divya Tadi  
**Project:** Helpdesk Performance & SLA Analytics  
**Tools:** SQL Server · Power BI · DAX · Python · Pandas · NumPy  
**Domain:** IT Operations · Helpdesk Analytics · SLA Management

- GitHub: [Add your repository URL here]
- LinkedIn: [Add your LinkedIn profile URL here]

## Acknowledgement

This repository is based on an existing project structure and has been modified for learning and portfolio purposes. Please retain appropriate credit to the original repository and comply with its licence. Add the original repository link here before publishing if required.

