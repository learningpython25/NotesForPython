##### 1. Can you explain the projects you worked on?
- Project Olympus - Invoice Extraction
	- Team 5- 6
	- 2 Months (Core Develope + 1.5 Months Infra)
	- Tech Stack: Python, Git in our PC, BitBucket, Agile, Scrum Master, JIRA, VMs + AWS (EC2 /EMR Instance)
	- Project Details: Daily - 200-300 files -> 1-100 Pages, Success Rate -> 95% 
	- Exception: They will be moved to a different folder for re-processing or user processing
	- It is in production -> 3 Issues ()
	- Python
- Backend ()

##### 2. Can you explain the entire life cycle of a project?

##### 3. Can you explain one project in detail?


## Invoice Extraction Project
"I built a Python automation script to process a folder of PDF invoices, extract key fields like date, invoice number, and amount using `pdfplumber` and regex, and write the data into a structured Excel file with `pandas`. It was designed to handle varying invoice formats, log errors, and allow easy scaling if more fields or formats are added."

- **Objective** – Developed a Python automation tool to process a folder of PDF invoices, extract up to 10 key fields (e.g., date, invoice number, vendor, amount), and store the data in an Excel file for reporting and analysis.
- **PDF Processing** – Utilized libraries like `PyPDF2`/`pdfplumber` to read text from each PDF and applied string matching & regex patterns to accurately locate field values despite layout variations.
- **Data Extraction Logic** – Designed a modular parsing function to handle different invoice formats, validate extracted fields, and handle missing or malformed data gracefully.
- **Excel Output** – Used `openpyxl`/`pandas` to write extracted data into a structured Excel sheet with column headers, ensuring clean formatting for further processing.
- **Automation & Scalability** – Implemented a loop to process all PDFs in a folder automatically, added error logging, and designed the code so new fields or formats can be added with minimal changes.
