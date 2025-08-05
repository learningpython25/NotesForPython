
### OS
- **`echo %PATH%`**
	- print the system environment variables

### Python
- **`where python`**
	- View all the python executable paths in the machine
	- `>>> C:\Python312\python.exe`
	
- **`which python`**
	- prints the major and minor python version
	- similar to `where python` but for UNIX flavored machines

- **`python --version`**
- **`python -V`**
	- `>>> Python 3.12.2`

- **`python -m site`**
	- shows all the listed site packages directories
### PIP
- **`pip --version`**
- **`pip --V`**
	- `>>> pip 24.0`
- **`pip list`**
	- shows the list of installed packages
- **`pip install <package_name>`**
	- installs the said package
- **`pip uninstall <package_name`**
	- uninstalls the package
- **`pip install pandas==1.3. 4`**
	- installs with version
- **`pip install --user <package_name>`**
	- installs only for the current user
- **`pip show pandas`**
	- shows all the details provided by the package author
- *`pip freeze > requirements.txt`*
	- when used within a venv, captures all the required packages for that environment
- *`pip install -r requirements.txt`*
	- inverse of the above, intalls from requirements.txt file