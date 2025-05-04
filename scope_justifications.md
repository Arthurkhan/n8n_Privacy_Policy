# API Scope Justifications

## Google Drive Scopes

### Drive API (https://www.googleapis.com/auth/drive)
**Justification:** This scope is necessary for the automation to access, read, and create files in the user's Google Drive. The automation will read existing documents to extract data for processing and create new files to store results from automated workflows. Limited to files explicitly selected by the user or created by the automation.

### Drive Metadata API (https://www.googleapis.com/auth/drive.metadata.readonly)
**Justification:** Required to list and search for files in the user's Drive without accessing their content. This enables the automation to locate specific files for processing without unnecessarily accessing file contents, preserving user privacy while maintaining functionality.

## Google Sheets Scopes

### Sheets API (https://www.googleapis.com/auth/spreadsheets)
**Justification:** Essential for the automation to create new spreadsheets, update existing ones, and append data to sheets as part of automated workflows. The automation will generate reports, track metrics, and maintain datasets by writing to spreadsheets specified by the user.

### Sheets Read API (https://www.googleapis.com/auth/spreadsheets.readonly)
**Justification:** Needed to read data from existing spreadsheets to use as input for automated workflows. This allows the automation to use spreadsheet data as parameters, conditions, or inputs for processing without modifying the original documents.

## Gmail Scopes

### Gmail Send API (https://www.googleapis.com/auth/gmail.send)
**Justification:** Required to send emails from the user's Gmail account as part of automated workflows. The automation will send notifications, alerts, and scheduled reports based on triggers and conditions defined by the user.

### Gmail Compose API (https://www.googleapis.com/auth/gmail.compose)
**Justification:** Necessary to create and save draft emails without sending them. This enables the automation to prepare emails for later review by the user before sending, especially for important communications that require human approval.

### Gmail Read API (https://www.googleapis.com/auth/gmail.readonly)
**Justification:** Essential for the automation to read emails to trigger workflows based on incoming messages. The automation will monitor specific email addresses, subjects, or contents to initiate automated processes like data extraction or response generation.

## Data Usage and Privacy Protection

All data accessed through these scopes will be:
- Used only for the specific automation tasks configured by the user
- Processed within the n8n workflow environment
- Not stored beyond the duration needed to complete the automated tasks
- Not shared with third parties except as explicitly configured by the user
- Protected using industry-standard security measures
