Automation Duplicate File Cleaner

Project Overview

Automation Duplicate File Cleaner is a Python-based automation tool designed to identify and remove duplicate files from a specified directory. It uses MD5 checksums to compare file contents, maintains activity logs, and sends an email report after the cleanup process.

The application also supports scheduled execution, allowing duplicate file cleanup to run automatically every day at 10:00 AM.

Features

- Duplicate File Detection: Identifies duplicate files by calculating MD5 checksums.
- Automated File Cleanup: Deletes extra copies while retaining the first file found for each group of duplicates.
- Scheduled Execution: Runs the cleanup process daily at 10:00 AM.
- Logging: Records scan activity, deleted files, errors, and execution status in a log file.
- Email Reports: Sends a cleanup report containing deleted file details and the total number of files deleted.
- Error Handling: Handles common file access and deletion errors.

Technologies Used

- Python 3
- OS and File System Operations
- MD5 Hashing
- Task Scheduling
- SMTP Email Automation
- Logging and Exception Handling

Project Files

- "Automation_DuplicateFile_Cleaner.py" — Main Python application.
- "duplicate_cleaner.log" — Log file generated automatically when the application runs.

How It Works

1. The program scans the configured directory.
2. It calculates the MD5 checksum of each accessible file.
3. Files with matching checksums are grouped as duplicates.
4. The program retains the first file in each group and attempts to delete the remaining copies.
5. It records the cleanup activity in a log file.
6. It sends an email report with the cleanup results.
7. It schedules the cleanup to run daily at 10:00 AM while the program remains running.

Configuration

Before running the program, configure the following settings in the Python file:

- "DirectoryName" — The directory to scan for duplicate files. The current configuration uses "Test".
- "SENDER_EMAIL" — The Gmail account used to send reports.
- "SENDER_PASSWORD" — The Gmail App Password used for SMTP authentication.
- "RECEIVER_EMAIL" — The email address that receives reports.

Security Note: Do not publish real email passwords or App Passwords in a public repository. Store credentials securely, preferably using environment variables.

How to Run

1. Install Python 3.

2. Install the required third-party package.

3. Configure the target directory and email settings.

4. Open a terminal in the project directory.

5. Run:
   
   "python Automation_DuplicateFile_Cleaner.py"

The program performs an initial cleanup and then continues running to execute the scheduled daily cleanup.

Important Notes

- Deleted duplicate files are removed permanently by the program; review and back up important files before running it.
- The configured "Test" directory must exist.
- The computer must remain on, and the Python program must remain running for the scheduled cleanup to execute.
- Gmail SMTP access must be configured correctly for email reports to be sent.

Future Enhancements

- Add a dry-run mode before deleting files.
- Allow users to select a directory interactively.
- Move email credentials to environment variables.
- Add configurable scheduling and improved reporting.


Requirements

Software Requirements

- Python 3.8 or later recommended.
- Windows, Linux, or macOS.
- Internet connectivity for sending email reports.
- A Gmail account configured for SMTP access.

Python Dependencies

Built-in Python modules:

- "sys"
- "os"
- "hashlib"
- "time"
- "smtplib"
- "logging"
- "datetime"
- "email.message"

These modules are included with Python and do not require separate installation.

Third-party package:

- "schedule" — Used to schedule the duplicate cleanup process.

Install Dependencies

Install Python from https://www.python.org/downloads/

Install the required third-party package using:

"python -m pip install schedule"

Verify the installation:

"python -m pip show schedule"

Email Configuration

- Configure a Gmail sender account.
- Generate and use a Gmail App Password if required.
- Set the sender and receiver email addresses in the program.
- Never commit passwords or other sensitive credentials to GitHub.

Directory Requirements

- Create a directory named "Test" in the program's working directory, or update the program to use your desired directory.
- Ensure the program has permission to read files and delete duplicates in the target directory.

Execution Requirements

- Keep the program running for the scheduled daily task to execute.
- The computer must remain powered on and awake at the scheduled time.


  author
  
  ragini mohite
  
