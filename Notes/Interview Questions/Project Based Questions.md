### 1. Can you explain one of your projects?

> [!NOTE] Answer
> ### National Grid Invoice Extraction
> **Where did you get this project from?:** There was a payments team in our firm which dealt with hundered PDF invoices where they had to extract the values like invoice amount and dates and others and feed it inot a downstream process. However, they were facing a lot of *redundancy* and *error* during this. Hence, we were asked to build a tool for them to handle this.
>
> **What is the project about? (Metadetails)** 
> *Duration:* 40+ Business Day (2 Months)
> *Team Size:* 3 Members  (Me, Av, Su)
> *Primary Language:* Python 
> *Tech Stack:* Python, Git (Local), Bitbucket, Agile Scrum, JIRA, AWS (EC2, EMR), Virtual Machines
>
> **High Level Design**
> 1. *Python -> Extraction Main Workflow*
>     - Implemented PDF parsing using `pdfPlumber` and **regex-based field matching** to handle different invoice layouts.
>     - Built **error handling** to identify incomplete or unreadable invoices and move them to an exceptions folder for **manual or automated reprocessing**.
> 2. *Development and Deployment*
>     - Used **Git** for source control and **Bitbucket** for code reviews.
>     - Created scripts to run in **AWS EC2** for large-scale batch processing.
>     - Worked in **Agile Scrum** environment — participated in sprint planning, daily standups, and retrospectives.
> 3. *Monitoring & Maintenance*
>     - Set up logging for tracking failed extractions.
>     - In production, resolved **3 post-deployment issues** related to regex mismatches and AWS instance configuration.
> 
> **Final Statistics**
> - Developed and deployed an automated system to process **3500+ invoice PDF files daily**, ranging from **45,000 pages each**.
> - Achieved **95% successful extraction rate** for up to 10 key fields per invoice (e.g., invoice number, date, amount, vendor).
> - Designed for scalability and currently running in **production** with minimal issues.



> [!abstract] Answer 2 - Simple
> ## Invoice Extraction Project
> "I built a Python automation script to process a folder of PDF invoices, extract key fields like date, invoice number, and amount using `pdfplumber` and regex, and write the data into a structured Excel file with `pandas`. It was designed to handle varying invoice formats, log errors, and allow easy scaling if more fields or formats are added."
> 
> - **Objective** – Developed a Python automation tool to process a folder of PDF invoices, extract up to 10 key fields (e.g., date, invoice number, vendor, amount), and store the data in an Excel file for reporting and analysis.
> - **PDF Processing** – Utilized libraries like `PyPDF2`/`pdfplumber` to read text from each PDF and applied string matching & regex patterns to accurately locate field values despite layout variations.
> - **Data Extraction Logic** – Designed a modular parsing function to handle different invoice formats, validate extracted fields, and handle missing or malformed data gracefully.
> - **Excel Output** – Used `openpyxl`/`pandas` to write extracted data into a structured Excel sheet with column headers, ensuring clean formatting for further processing.
> - **Automation & Scalability** – Implemented a loop to process all PDFs in a folder automatically, added error logging, and designed the code so new fields or formats can be added with minimal changes.

### 2. Can you explain the entire life cycle of a project?

> [!NOTE]
> 1. **Requirement Gathering & Understanding**
> 
>    * For this project, the requirement was: *“Check all files in a folder and return only valid PDFs (files ending with `.pdf` and with size > 0).”*
>    * At this stage, I clarify the scope, edge cases (like empty files, subfolders), and success criteria.
> 
> 2. **Solution Design**
> 
>    * I decide what modules or functions I’ll need.
>    * For example:
> 
>      * A function to list files.
>      * A function to validate each file.
>      * Some basic logging.
>    * I also choose the tools (in this case, Python + `os` module for filesystem).
> 
> 3. **Implementation (Coding)**
> 
>    * Write the Python function `find_valid_pdfs()`.
>    * Add error handling with `try/except`.
>    * Add logging using `print()` statements.
>    * Keep the code simple so beginners can understand.
> 
> 4. **Testing**
> 
>    * Run the script with different cases:
> 
>      * A folder with only PDFs.
>      * A folder with non-PDFs.
>      * Empty PDFs (0 KB).
>      * Subfolders mixed in.
>    * Confirm that the function only returns the valid files.
> 
> 5. **Deployment / Delivery**
> 
>    * Share the script with the team or package it for others to use.
>    * Maybe configure it so that the folder path can be passed dynamically.
> 
> 6. **Maintenance / Improvements**
> 
>    * Later, if the requirements change (for example, check `.docx` files too, or add logging to a file instead of console), I can extend the same script.
>    * Maintenance usually means fixing bugs or enhancing features based on feedback.

### 3. Can you tell about the difficulties you faced in this process?

Problem -> Effect -> Resolution

> [!NOTE]
> 1. **Handling Non-File Items in the Folder**
>    * At first, I assumed all the required files were placed inside a directory, however during production we learned that there were *junk files* and also there *nested folders*. That caused the tool to either *fail* or *miss files*
>    * **Solution:** I built a small logic to flatten out all the nested folders and the also to remove the junk files using the `os` and `path` python libraries
> 
> 2. **Invalid file or Invalid Layout**
> 
>    * Once it was live, there were some files which looked like .pdf files but was *invalid* and when the code tried to read them they would throw errors; and sometimes the *layout* was different and this lead to *incorrect values*.
>    * **Solution:** We added *two validations* to check if the file was a valid pdf and to check if it aligned with a pre-defined layout. (pdfplumber -> open, keyword -> invoice)




# New Projects

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

---

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

### Smaller version


> [!NOTE]
> ### Project 2: Metrics API Dashboard
> 
> * Developed a **Python-based API service (FastAPI)** with 8 endpoints to deliver **real-time KPIs** sourced from both files (CSV/Excel) and SQL database.
> * Implemented **filtering, sorting, and search** at endpoint level to support flexible dashboards.
> * Containerized with **Docker** and deployed on **AWS EC2**, integrated with Power BI for visualization.
> * Improved reporting cycle from **2–3 days to daily refresh**, reducing manual report generation by **70%**.
> 

> [!NOTE]
> ### Project 3: National Grid Procurement Analytics
> 
> * Analyzed **12 months (\~3M rows)** of procurement data (PO → Invoice → Payment) for vendor performance monitoring.
> * Built Python-based analytics pipeline with **Pandas, NumPy, Matplotlib, Seaborn** to detect **delays and bottlenecks**.
> * Identified a **3x increase in invoice-to-payment delays**, causing a **40% drop in vendor delivery volume**.
> * Delivered vendor performance dashboards and **data-backed recommendations** that informed contract renegotiations.

