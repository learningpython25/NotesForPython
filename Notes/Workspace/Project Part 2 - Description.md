#### Part 2
For each file
- ~~Open that file -> pdf (pdfplumber, pymupdf(fitz))~~
- ~~Grab all the text (copy all the text) = ~~
- ~~write to text file~~
- ~~read the text file -> str~~
~~- using *re*  from the string -> grab all the values
	- invoice amount
	- invoice date
	- Due Date
	- Total Amount~~
- ~~Write to excel (csv) [delimiter = comma, tab]~~

Input: 3 pdf files
output: extracted_invoice_details.csv
- headers: Id, file_name, processed_date, Invoice Number, Invoice Amount, Due Date, Total Due

### Major Actions
- reading pdf file and getting text
- writing to text file and reading back (for audit and future purpose)
- getting values using `re` -> invoice amount, invoice date, due date, total due
- write ouput to csv 


#### reading or writing a text file
.txt, csv files (table format)

**open(file_path, mode = r, w, a ,.  encoding=None)**
- read
	- readline
	- readlines
- write
	- write
	- writelines
- append


**regular expression**
`\d` -> matches any digit
`\w` -> matche any alphabet or digit
`\s` -> matches space

`\D` -> matchs any not a digit
`\W`
`\S`

`*` -> zero or more of previous
`?` -> zero or one of previous
`+` -> one or more of previous