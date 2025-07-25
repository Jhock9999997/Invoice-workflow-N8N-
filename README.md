# Invoice-workflow-N8N-
This workflow automates the end-to-end handling of incoming invoices using a combination of Google Drive, AI-based information extraction, Google Sheets, and Gmail.

Workflow Overview
The system detects newly uploaded invoice files in a designated Google Drive folder. It extracts key invoice details regardless of formatting. It then logs them into a Google Sheets database. Finally, it uses AI to generate a summary email, which is sent directly to the billing team.

<img width="1298" height="358" alt="image" src="https://github.com/user-attachments/assets/e8e78e79-e4b7-4482-9472-461d12b8ca28" />


Automated Invoice Processing Workflow (n8n)
This workflow automates the end-to-end handling of incoming invoices using a combination of Google Drive, AI-based information extraction, Google Sheets, and Gmail.

Workflow Overview
The system detects newly uploaded invoice files in a designated Google Drive folder. It extracts key invoice details—regardless of formatting—then logs them into a Google Sheets database. Finally, it uses AI to generate a summary email, which is sent directly to the billing team.

Step-by-Step Process
1. Google Drive Trigger
The workflow is triggered whenever a new file is added to a specific Google Drive folder.

2. Download Binary
The file (typically a PDF invoice) is downloaded in binary format for processing.

3. Extract from PDF
The file content is extracted regardless of formatting inconsistencies, preparing it for structured analysis.

4. Information Extraction (via OpenAI)
An AI model processes the raw text and accurately identifies and extracts key fields:

- Client name

- Invoice number

- Invoice date

- Due date

- Total amount

- Client phone

- Client address

- Client email

5. Update Database (Google Sheets)
The extracted data is automatically appended or updated in a Google Sheets invoice log for record-keeping and future reference.

6. Create Email (OpenAI)
An OpenAI-powered node drafts a clear, professional message summarizing the invoice details for internal review.

7. Send to Billing Team (Gmail)
The generated email is sent to the billing team, ensuring timely review and processing of each invoice.

8. No Operation (End Node)
The workflow ends cleanly after the email is dispatched.

This automation significantly reduces manual effort, improves consistency in record keeping, and ensures that all invoices are reviewed and actioned promptly by the appropriate team.
