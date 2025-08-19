### 1. Can you explain some of your projects?

> [!NOTE] Answer
> ### National Grid Invoice Extraction
> **Requirement Gathering:** There was a payments team in our firm which dealt with hundered PDF invoices where they had to extract the values like invoice amount and dates and others and feed it inot a downstream process. However, they were facing a lot of redundancy and error during this. Hence, we were asked to build a tool for them to handle this.
> 
> **Duration:** 2 Months (Core Development) + 1.5 Months (Infrastructure Setup)  
> **Team Size:** 2-3 Members  
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

### 2. Can you explain the entire life cycle of a project?

> [!NOTE]
> 1. **Requirement Gathering & Understanding**
> 
>    * For this project, the requirement was: *“Check all files in a folder and return only valid PDFs (files ending with `.pdf` and with size > 0).”*
>    * At this stage, I clarify the scope, edge cases (like empty files, subfolders), and success criteria.
> 
> 2. **Planning & Design**
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

> [!NOTE]
> 1. **Handling Non-File Items in the Folder**
> 
>    * At first, I assumed everything in the folder was a file, but some folders contained sub-directories.
>    * This caused errors when I tried to check file size.
>    * **Solution:** I used `os.path.isfile()` to filter out subfolders before validation.
> 
> 2. **Case Sensitivity of File Extensions**
> 
>    * Initially, my script only checked for `.pdf`. Files with `.PDF` or `.Pdf` were skipped even though they were valid.
>    * **Solution:** I normalized the filename using `.lower()` before checking the extension.
> 
> 3. **Error Handling & Logging**
> 
>    * When I first ran the script, if one file was locked or corrupted, the whole program crashed.
>    * **Solution:** I added `try/except` around file operations and simple logging using `print()` so that errors are shown but processing continues for other files.
> 