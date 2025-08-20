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




