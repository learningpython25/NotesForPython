```py
import os

def find_valid_files(folder_path):
    """
    Find all the valid PDF files in a given folder
    Check if file is PDF or not
    Check if the file size > 0
    Return the valid files as a list
    """
    
    valid_files = []
    
    # Get all files in the folder
    files = os.listdir(folder_path)
    print(f'===> Total files: {len(files)}\nItems in folder: {files}')
    try: 
        for file_name in files: 
            file_path = os.path.join(folder_path, file_name)
            
            # CHECK 3 - Is it a file or folder?
            if not os.path.isfile(file_path):
                print(f'Skipping: {file_name} (not a FILE)')
                continue
            
            # CHECK 1 - Is file a PDF?        
            if not file_name.lower().endswith(".pdf"):
                print(f'Skipping: {file_name} (not a pdf)')
                continue

            # CHEK 2 - Is file size > 0
            if os.path.getsize(file_path) == 0:
                print(f'Skipping: {file_name} (size is 0)')
                continue
            
            valid_files.append(file_path)
            print(f'Valid file: {file_name}')
        return valid_files
    except Exception as e: 
        print(f'Error while validating: {e}')

# MAIN
if __name__ == "__main__":
    print("Process Started")
    input_folder = r"<your path>\workspace\project_1\input_files"
    valid_files = find_valid_files(input_folder)
    print(f'===> Total Valid files: {len(valid_files)}')
    print("Process Completed")
 
```