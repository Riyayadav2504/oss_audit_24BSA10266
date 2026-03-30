# oss_audit_24BSA10266
A Capstone Project for Open Source Software

Student Details
Name: Riya Yadav
Registration Number: 24BSA10266
Course: Open Source Software
About the Project

This project is a detailed audit of the Apache HTTP Server, one of the most widely used open-source web servers. The goal was not just to study Apache theoretically, but also to understand how open-source systems work in practice.

The report explores how Apache evolved over time, the ideas behind its licensing (Apache License 2.0), and the role of its community. It also briefly compares Apache with proprietary web servers to highlight the differences in flexibility and control.

To make things more practical, I created five Bash scripts that simulate real-world system administration tasks. These scripts helped me apply concepts like file handling, log analysis, and system inspection using Linux tools.

Tools and Technologies Used
Operating System: Kali Linux / Ubuntu
Shell: Bash (/bin/bash)
Web Server: Apache HTTP Server (apache2)
Package Manager: apt
Utilities: uname, whoami, dpkg, du, grep, awk, date, uptime
Project Structure
open-source-audit-apache/

├── script1.sh          # System Identity Report  
├── script2.sh          # FOSS Package Inspector  
├── script3.sh          # Disk and Permission Auditor  
├── script4.sh          # Log File Analyzer  
├── script5.sh          # Open Source Manifesto Generator  

└── README.md           # Documentation  
Setup Guide

Before running the scripts, make sure you're using a Debian-based Linux system like Ubuntu or Kali.

Step 1: Update packages
sudo apt update
Step 2: Install Apache
sudo apt install apache2 -y
Step 3: Check installation
apache2 -v
Step 4: Give execute permission to scripts
chmod +x script1.sh script2.sh script3.sh script4.sh script5.sh
Running the Scripts
Script	Command
script1.sh	./script1.sh
script2.sh	./script2.sh
script3.sh	./script3.sh
script4.sh	./script4.sh /var/log/apache2/error.log error
script5.sh	./script5.sh

Note:
script4.sh takes two inputs:

Log file path
Keyword (optional, default = "error")
What Each Script Does
script1.sh – System Identity Report
Displays basic system information like kernel version, current user, OS details, uptime, and date.
script2.sh – FOSS Package Inspector
Checks if Apache is installed and shows package details. It also prints a small note based on the package using a case statement.
script3.sh – Disk and Permission Auditor
Goes through important system directories and shows permissions, ownership, and disk usage. It also checks Apache’s config directory.
script4.sh – Log File Analyzer
Reads a log file, searches for a keyword, counts occurrences, and shows the last five matching lines.
script5.sh – Open Source Manifesto Generator
Takes user input and creates a personalised manifesto file based on system details and responses.
Output Overview

Each script produces a different type of output:

script1.sh → A simple system info dashboard
script2.sh → Apache installation status and package info
script3.sh → Directory audit table
script4.sh → Log analysis summary
script5.sh → A generated manifesto saved as a .txt file
Concepts Applied

While working on these scripts, I used several core Linux and shell scripting concepts:

Variables and system commands
User input handling (read)
Conditional statements (if-else)
Case statements
Loops (for, while)
Command-line arguments ($1, $2)
File handling and redirection
Text processing tools like grep, awk, tail
Basic error handling and exit codes
Notes
These scripts are designed for Linux systems only.
Make sure scripts have execute permission before running.
Some commands (especially in script3) may need sudo for accurate results.
For testing script4, you can also use:
/var/log/syslog (Ubuntu)
/var/log/kern.log (Kali)

The manifesto file is saved as:

manifesto_<username>.txt
Final Thoughts

This project gave me a better understanding of how open-source software works beyond just theory. Working with Apache and writing scripts helped me see how transparency and flexibility actually play out in real systems.

Overall, it was a good mix of research and hands-on practice, and it helped me get more comfortable with Linux and shell scripting.
