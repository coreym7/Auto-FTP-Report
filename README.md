# Automating FTP Report Sharing: Streamlining Regular Data Transfers with Python

## Problem Statement
In this project, we aimed to automate the retrieval of reports from an FTP site and subsequent email distribution to a selected group of recipients. Previously, this repetitive and time-consuming task had been performed manually, presenting an opportunity for automation.

## Technologies Used
Python, with its cross-platform compatibility, comprehensive library ecosystem, and readability, was the primary technology used for this project. The Python libraries used in the project included `ftplib`, `smtplib`, `email`, and `ftputil`, each serving distinct roles in FTP connection, email composition, and sending functionalities.

## Strategy and Approach
The developed automation script follows these main steps:

1. **FTP Connection and Report Download**: Using the `ftplib` and `ftputil` libraries, the script establishes a connection with the FTP server, downloads the specified report, and includes error checking mechanisms to validate the report's existence on the server before initiating the download.
   
2. **Email Composition and Sending**: Next, the script composes an email, attaches the downloaded report, and dispatches it to a designated group of recipients. This is achieved using the `smtplib` and `email` libraries.
   
3. **Scheduling**: To facilitate automatic and periodic execution, the script is scheduled using an appropriate task scheduler: Task Scheduler for Windows and cron for Linux/macOS systems.

## Results
The automation script effectively removed the need for manual intervention in the process of report retrieval and distribution, thereby saving considerable time and effort. It also demonstrated the utility of Python as a tool for automating routine tasks, while maintaining a high level of reliability.

## Learnings and Challenges
One of the main challenges in this project was managing dependencies and packages in Python. However, this also served as a valuable learning experience in managing different Python environments and versions. The secure storage of credentials and the effective handling of errors and exceptions were important aspects of creating a robust and reliable automation process.

## Future Improvements
While this project achieved the primary objective, there are potential areas for improvement and expansion. The additional check to verify the downloaded report is from the last 24 hours is due to issues where the 3rd party client that has scripts in place to place the report here to be downloaded has had issues preventing a new report from being available. A possible improvement to this could be to write in a fallback measure to access the site directly, create a user session and then access the report URL directly and handle the received file. 

## Impact
This automation solution has significantly streamlined the process of report retrieval and distribution. By replacing the manual, repetitive task, we have seen improved efficiency and reduced human error, freeing up valuable time for staff to engage in more critical tasks.
