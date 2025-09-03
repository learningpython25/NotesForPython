#### AWS

boto3 -> 

boto3 -> boto3.my_files/file.pdf

Amazon Web Services (2002)

VMs -> EC2 (windows, *linux*) t1, t3, 
files -> Simple Storage Service (S3 buckets)
computations -> lambda (python, js, java -> runtime)

route 53 -> 
cloud front ->
load balancer

RDS() -> dynamo db

IAM (identity and access management)
Cloud Watch -> monitroing

**Project 2**

API -> 

MVC -> frontend, backed -> full stack

API

backend -> database + logic
Frontend -> web, reac 

story: 

**Project 3**
data analytics
story: 500 items -> stage + time -> delays

profit: 123k,456
loss: 43134123
vendors: 1341

different sources: databases, excel files, pdf files, notepad, 

step 1: gather data
step 2: set the data for consumption (12 KPI)

API -> json (12)

> [!abstract]
> ## Project 2: Metrics API Dashboard
> 
> **Where did you get this project from?:**
> There was a Business Insights team that wanted a **dashboard** to track KPIs. The challenge was that the metrics were not in one place — some came from **uploaded files** (CSV, Excel) while others came from an **internal SQL database**. They wanted a **Python-based API service** that would expose these metrics via endpoints, so their dashboard could consume them.
> 
> **Project Details (Metadetails):**
> 
> * *Duration:* 5–6 Weeks
> * *Team Size:* 2 Members (Me, Ka)
> * *Primary Language:* Python
> * *Tech Stack:* Python (FastAPI/Flask, Pandas, SQLAlchemy), PostgreSQL, GitHub, Docker, AWS EC2, Agile Scrum
> 
> **High Level Design (6–8 Steps):**
> 
> 1. **Requirement Gathering & Analysis**
> 
>    * Identified **6–8 key metrics** (e.g., revenue growth, churn rate, customer retention).
>    * Understood data sources: daily CSV uploads and SQL tables.
> 2. **Data Ingestion & Pre-processing**
> 
>    * Wrote **Python ETL scripts** using Pandas to clean uploaded files.
>    * Connected to PostgreSQL via SQLAlchemy to fetch transactional data.
> 3. **Metric Computation Layer**
> 
>    * Implemented functions for **aggregations, trends, and derived KPIs**.
>    * Added **filters, sorting, and search capabilities** for more flexibility.
> 4. **API Development**
> 
>    * Built **FastAPI endpoints**: each endpoint corresponds to one metric.
>    * Defined request parameters for filters (date range, vendor, category).
> 5. **Testing & Validation**
> 
>    * Unit-tested each endpoint with pytest.
>    * Conducted data validation with sample dashboards.
> 6. **Deployment & Hosting**
> 
>    * Containerized API using Docker.
>    * Deployed on **AWS EC2** and connected to the BI dashboard team.
> 7. **Agile Workflow**
> 
>    * Worked in **2-week sprints**, demoing endpoints at sprint reviews.
>    * Used GitHub + Jira for code review and task tracking.
> 8. **Monitoring & Maintenance**
> 
>    * Added **logging & error handling** for failed file loads or DB timeouts.
>    * Setup auto-restart scripts for API in case of crashes.
> 
> **Final Statistics:**
> 
> * Delivered **8 REST APIs** with filters & sorting.
> * Dashboard team integrated APIs in **Power BI**, improving data refresh from **2–3 days to near real-time (daily)**.
> * Reduced manual report generation effort by **70%**.


> [!faq]
> ## Project 3: National Grid Procurement Analytics
> 
> **Where did you get this project from?:**
> National Grid’s **procurement team** wanted to investigate why a key vendor’s orders had **dropped significantly** compared to the past. They provided **12 months of purchase-to-payment data** and wanted insights into **where delays were happening** (purchase order → invoice → payment settlement).
> 
> **Project Details (Metadetails):**
> 
> * *Duration:* 2.5 Months
> * *Team Size:* 3 Members (Me, Su, Ar)
> * *Primary Language:* Python
> * *Tech Stack:* Python (Pandas, NumPy, Matplotlib, Seaborn), PostgreSQL, Jupyter, GitLab, Agile Scrum
> 
> **High Level Design (6–9 Steps):**
> 
> 1. **Data Collection & Understanding**
> 
>    * Collected **12 months of procurement logs** (POs, GRNs, Invoices, Payments).
>    * Size: \~3M rows across multiple CSVs and DB extracts.
> 2. **Data Cleaning & Preprocessing**
> 
>    * Standardized date formats, vendor codes, PO numbers.
>    * Removed duplicate or canceled orders.
> 3. **Exploratory Data Analysis (EDA)**
> 
>    * Identified process bottlenecks (average lead time per step).
>    * Visualized trends in order quantities and vendor delays.
> 4. **Metric Computation**
> 
>    * Calculated **cycle times**: PO → Approval → Invoice → Payment.
>    * Segmented by vendor, category, and month.
> 5. **Vendor Performance Comparison**
> 
>    * Compared the target vendor vs. peers.
>    * Detected a **3x increase in invoice-to-payment delays** over the past 6 months.
> 6. **Root Cause Analysis**
> 
>    * Correlated delays with **contract changes, late invoice submissions, and manual re-approvals**.
>    * Found **holiday season spikes** also worsened timelines.
> 7. **Visualization & Dashboarding**
> 
>    * Created plots (trend lines, histograms, vendor comparisons).
>    * Shared outputs via Jupyter notebooks and exported interactive plots.
> 8. **Collaboration & Workflow**
> 
>    * Split roles: data cleaning (Su), analytics modeling (me), visualization/reporting (Ar).
>    * Followed Agile sprints with 2-week deliverables.
> 9. **Final Report & Delivery**
> 
>    * Submitted findings with **data-backed insights** and vendor-specific recommendations.
> 
> **Final Statistics:**
> 
> * Processed and analyzed **3M+ records** across 12 months.
> * Identified that **invoice approval & payment settlement delays** caused a **40% drop in vendor delivery volume**.
> * Helped procurement team renegotiate terms and streamline approvals.