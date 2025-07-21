# MSTR_User_deletion-
#### tableau_user_unlicensing
Script to Change the User Site role to unlicensed if found inactive for given number of days

Case1 : Didn't login in last 60 days, user will be removed from Groups and Unlicensed 
	    - Will not be able to Login



SET Environment variable based on the env the code will run
For Windows Go to advanced system settings -> Advanced tab -> Environment Variables -> System Variables -> add new variable 'Stage' with value 'Dev' or 'QA' or 'Prod'

install required python packages listed under local_debug_requirements.txt if not installed already

ex: pip install mstrio-py 
    or
    pip install -r local_debug/local_debug_requirements.txt 

****For temporary session to test****
powershell -> $env:Stage="Dev" // $env:Stage="QA" // $env:Stage="Prod"
****For temporary session to test****


Based on the Stage Environment variable respecive config json file will be referred/loaded
Follow Below steps for Debugging Locally

    Create a venv (virtual environment) to debug locally
    >> python -m venv src-python\unlicensing_script\local_debug

python -m venv local_debug

    Select Python interper with local debug venv 
    Press CTRL + SHIFT + P 
    >> Python: Select Interpreter

    Select Virtual Environment created under local_debug
    'local_debug':venv

    Reload Window Press "CTRL+SHIFT+P"

    Create Terminal for Python
    Press CTRL + SHIFT + P 
    >> Python: Create Terminal

    Reload Window Press "CTRL+SHIFT+P"

    Install required pip libraries from local_debug_requirements.txt
    >> python -m pip install --upgrade pip
    >> pip install -r src-python\unlicensing_script\local_debug_requirements.txt

######
