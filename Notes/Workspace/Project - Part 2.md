```python
import fitz
import re 
import csv
import os


def extract_text_from_pdf(pdf_path) -> str:
    pdf_text = ""
    print(f"Reading the pdf file: {pdf_path}")
    
    doc = fitz.open(pdf_path)
    for page in doc:
        pdf_text += page.get_text()
    doc.close()    
    print("Successfully read the pdf file")
    return pdf_text

def save_to_text_file(pdf_path, text) -> str:    
    folder = os.path.dirname(pdf_path)
    base_name = os.path.splitext(os.path.basename(pdf_path))[0]
    
    txt_file_name = f"{base_name}.txt"
    txt_file_path = os.path.join(folder, txt_file_name)
    print(f"Writing text to the file: {txt_file_name}")
    
    with open(txt_file_path, mode='w', encoding=None) as f:
        f.write(text)
    print("Successfully written")
    
    return txt_file_path

def extract_invoice_details(text, file_name) -> dict:
    
    
    invoice_number = re.search( r"Invoice Number\n(.*)" , text)
    invoice_date = re.search( r"Invoice Date\n(.*)" , text)
    due_date = re.search( r"Due Date\n(.*)" , text)
    total_due = re.search( r"Total Due\n(.*)" , text)
    
    print(invoice_number.group(1), invoice_date.group(1))
    
    details = {
        "File Name": file_name,
        "Invoice Number": invoice_number.group(1),
        "Invoice Date": invoice_date.group(1),
        "Due Date": due_date.group(1),
        "Total Due": total_due.group(1)
    }
    
    print("Successfully extracted the values")
    return details

def save_to_csv(pdf_path, details):
    folder = os.path.dirname(pdf_path)
    base_name = os.path.splitext(os.path.basename(pdf_path))[0]
    
    csv_file_name = f"{base_name}.csv"
    csv_file_path = os.path.join(folder, csv_file_name)
    print(f"Writing OUTPUT to the file: {csv_file_path}")
    
    with open(csv_file_path, "a", encoding=None) as csvfile:
        writer = csv.DictWriter(csvfile, fieldnames=details.keys())
        writer.writeheader()
        writer.writerow(details)

    pass


if __name__ == "__main__":
    print("process started")
    pdf_file_path = r"D:\steve\my study\student\workspace\project_1\input_files\HotFolder\one.pdf"
    
    #Action 1
    text = extract_text_from_pdf(pdf_file_path)
    
    #Action 2
    save_to_text_file(pdf_file_path, text)
    
    #Action 3
    invoice_details = extract_invoice_details(text, os.path.basename(pdf_file_path))
    
    #Action 4
    save_to_csv(pdf_file_path, invoice_details)
    
    
    print("process completed")
```