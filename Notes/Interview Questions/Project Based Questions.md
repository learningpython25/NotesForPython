##### 1. Can you explain some of your projects?

> [!NOTE] Answer
> ###### Project Olympus – Invoice Extraction Automation
> 
> **Duration:** 2 Months (Core Development) + 1.5 Months (Infrastructure Setup)  
> **Team Size:** 5–6 Members  
> **Role:** Python Developer  
> **Tech Stack:** Python, Git (Local), Bitbucket, Agile Scrum, JIRA, AWS (EC2, EMR), Virtual Machines
> 
> **Overview**
> - Developed and deployed an automated system to process **200–300 invoice PDF files daily**, ranging from **1 to 100 pages each**.
> - Achieved **95% successful extraction rate** for up to 10 key fields per invoice (e.g., invoice number, date, amount, vendor).
> - Designed for scalability and currently running in **production** with minimal issues.
> 
> **Core Responsibilities**
> 1. *PDF Data Extraction*
>     - Implemented PDF parsing using `pdfplumber` and **regex-based field matching** to handle different invoice layouts.
>     - Built **error handling** to identify incomplete or unreadable invoices and move them to an exceptions folder for **manual or automated reprocessing**.
> 2. *Workflow*
>     - Created scripts to run in **AWS EC2** for large-scale batch processing.
>     - Integrated with **AWS EMR** for potential distributed processing of high-volume workloads.
> 3. *Collaboration & Version Control*
>     - Used **Git** for source control and **Bitbucket** for code reviews.
>     - Worked in **Agile Scrum** environment — participated in sprint planning, daily standups, and retrospectives.
> 4. *Monitoring & Maintenance*
>     - Set up logging for tracking failed extractions.
>     - In production, resolved **3 post-deployment issues** related to regex mismatches and AWS instance configuration.
> 5. *Infrastructure Setup*
>     - Helped configure **VM environments** for development and testing.
>     - Coordinated with DevOps for AWS deployment and scaling.

> [!abstract] Answer 2 - Simple
> ## Invoice Extraction Project
> "I built a Python automation script to process a folder of PDF invoices, extract key fields like date, invoice number, and amount using `pdfplumber` and regex, and write the data into a structured Excel file with `pandas`. It was designed to handle varying invoice formats, log errors, and allow easy scaling if more fields or formats are added."
> 
> - **Objective** – Developed a Python automation tool to process a folder of PDF invoices, extract up to 10 key fields (e.g., date, invoice number, vendor, amount), and store the data in an Excel file for reporting and analysis.
> - **PDF Processing** – Utilized libraries like `PyPDF2`/`pdfplumber` to read text from each PDF and applied string matching & regex patterns to accurately locate field values despite layout variations.
> - **Data Extraction Logic** – Designed a modular parsing function to handle different invoice formats, validate extracted fields, and handle missing or malformed data gracefully.
> - **Excel Output** – Used `openpyxl`/`pandas` to write extracted data into a structured Excel sheet with column headers, ensuring clean formatting for further processing.
> - **Automation & Scalability** – Implemented a loop to process all PDFs in a folder automatically, added error logging, and designed the code so new fields or formats can be added with minimal changes.

##### 2. Can you explain the entire life cycle of a project?

##### 3. Can you explain one project in detail?

