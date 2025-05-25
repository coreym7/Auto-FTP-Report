# Auto FTP Report: Streamlining Scheduled Data Transfers with Python

## Impact
This automation replaced a manual, repetitive process of downloading reports from an FTP server and distributing them via email. It saved time, reduced errors, and allowed staff to focus on more critical tasks.

## Problem
The previous process required team members to manually log into an FTP site, retrieve a report, and send it via email to internal stakeholders. This created inefficiencies and room for inconsistency.

## Technology Stack
- Python
- `paramiko`, `ftplib` – FTP + SFTP access
- `smtplib`, `email` – Email delivery
- `pandas`, `openpyxl` – Data conversion (CSV → Excel)
- Logging, `cron` / Windows Task Scheduler for automation

## Solution Overview
1. **FTP Access + Download**  
   Connects to a remote FTP or SFTP server, verifies the file exists and was updated in the last 24 hours, and downloads it to a local directory.

2. **Conversion**  
   Transforms the report from CSV to Excel with auto-formatting for readability.

3. **Email Delivery (Optional)**  
   [Functionality was scoped but not implemented in this version — original intent included email attachments via SMTP.]

4. **Scheduled Execution**  
   Designed to run via OS-level task schedulers.

## Lessons + Engineering Decisions
- Managing secure credentials and connection logic across protocols (FTP/SFTP)
- Ensured timestamp-based validation of file freshness
- Implemented safe logging + exception handling
- Chose modular structure to enable future email integration

## Future Improvements
- Add web session fallback (via `requests` or browser automation) in case the FTP upload fails
- Add optional email attachment logic
- Allow dynamic file selection or pattern-matching for filename parsing

## Status
✅ Working script  
⚠️ Email and web session fallback not implemented yet

