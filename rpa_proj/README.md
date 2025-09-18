# Hired Candidates Email Automation

A UiPath automation workflow that processes hired candidates from an Excel file and sends offer letters via email.

## What it does

1. **Reads candidate data** from an Excel file (Status sheet)
2. **Filters hired candidates** (Status = "Hired")
3. **Sends personalized offer letters** via Outlook 365
4. **Updates process status** in Excel
5. **Adds candidates to queue** for further processing

## Prerequisites

- UiPath Studio
- Excel file with candidate data
- Outlook 365 account configured
- UiPath Orchestrator access (for queue operations)

## Setup

1. **Excel File**: Ensure your Excel file has a "Status" sheet with columns:
   - CandidateID
   - Name
   - Email
   - Status

2. **Asset Configuration**: Create a robot asset named `Excelpathfile` with the path to your Excel file

3. **Email Template**: Place your offer letter template at `Data\Templates\OfferLetter.txt`

4. **Queue Setup**: Create a queue named "Hireddata" in UiPath Orchestrator

## Configuration

- **Email Account**: Update the email address in the workflow (currently set to `22cse033@bnmit.in`)
- **Workspace**: Adjust the folder path for your UiPath workspace

## Output

- Hired candidates receive personalized offer letters
- Excel file is updated with "Added to Queue" status
- Candidate data is added to the processing queue

## Error Handling


The workflow includes comprehensive error handling with logging for troubleshooting any issues during execution.
