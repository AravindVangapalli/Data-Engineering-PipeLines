# To Create .gitignore file use this 
--> echo myenv/ > .gitignore


# 
Step 1: Install Git for Windows

1. Go to the official website: git-scm.com
2. Click on Click here to download to get the latest 64-bit standalone installer.
3. Run the downloaded .exe file.
4. Keep clicking Next through the setup installer using the default settings (the defaults are exactly what you need). Click Install at the end.

# Initialize this folder as a Git repository
git init

# Track all your project folders and files (except what we ignored)
git add .

# Save your snapshot locally
git commit -m "Initial commit of Demo-ETL pipeline"

# Set the main branch name
git branch -M main

# Link your local project to your GitHub repository URL
# (Replace the URL below with your actual GitHub repository URL)
git remote add origin https://github.com

# Push everything up directly to the main branch
git push -u origin main

extract.py --> Responsible for:
    Creating SparkSession
    Reading the source data

transform.py --> Responsible for:
    Cleaning
    Standardizings
    Casting
    Date conversion
    String normalization
    Null normalization

validate.py --> Responsible for:
    Data-quality rules
    Required fields
    Amount validation
    Date validation
    Currency validation
    Valid/rejected records

main.py --> Responsible for:
    Extract --> Profile --> Transform --> Validate --> Write
    It should not contain all the actual cleaning logic.














