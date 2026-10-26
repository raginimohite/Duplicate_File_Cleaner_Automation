Duplicate File Cleaner Automation

Project Description

This Python automation project identifies and deletes duplicate files from a specified directory using MD5 checksums. It also sends an email report after cleanup and schedules the task to run daily at 10:00 AM.

Features

- Detects duplicate files using MD5 checksum.
- Deletes duplicate files while keeping one copy.
- Generates logs of cleanup activities.
- Sends an email report after cleanup.
- Schedules automatic daily cleanup.

Technologies Used

- Python
- OS and Hashlib modules
- Schedule module
- SMTP and EmailMessage
- Logging module

How to Run

1. Install the required package:
   "pip install -r requirements.txt"
2. Configure email credentials.
3. Set the target directory in the code.
4. Run the script:
   "python main.py"

Note

Use a test directory first. The script permanently deletes duplicate files. Configure Gmail App Password securely before sending emails.


  
