# Invoice-workflow-N8N-
This workflow automates the end-to-end handling of incoming invoices using a combination of Google Drive, AI-based information extraction, Google Sheets, and Gmail.

**Workflow Overview:

The system detects newly uploaded invoice files in a designated Google Drive folder. It extracts key invoice details regardless of formatting. It then logs them into a Google Sheets database. Finally, it uses AI to generate a summary email, which is sent directly to the billing team.

<img width="1032" height="554" alt="image" src="https://github.com/user-attachments/assets/08bd8387-dc15-4144-9898-3fddb945793f" />



**Automated Invoice Processing Workflow (n8n):

This workflow automates the end-to-end handling of incoming invoices using a combination of Google Drive, AI-based information extraction, Google Sheets, and Gmail.


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

**Final Result:

The system outputs a clear and professional email sent to the billing team, summarizing the invoice details and providing a link to the updated database. Below is an example of a generated email:

<img width="1412" height="822" alt="image" src="https://github.com/user-attachments/assets/b19d5010-568b-4450-ac70-746608cf9ba0" />

