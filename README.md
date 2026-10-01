# 📋 Google Apps Script Dynamic List Automator

A robust Google Apps Script designed to automate the generation of official categorized reports and rosters. This script cross-references data between multiple Google Sheets, filters records based on conditional business logic (e.g., cohort and status), and dynamically populates structured tables within a Google Doc template.

## ✨ Features

- **📊 Data Cross-Referencing:** Automatically searches and merges data from a Master Sheet with an external database (e.g., scores, grades, or external statuses) using unique identifiers (ID, Email, or Name).
- **🔀 Smart Filtering & Routing:** Evaluates row data and separates records into distinct arrays based on their conditional status (e.g., "Finalized" vs. "Pending") and specific cohorts.
- **📄 Dynamic Table Generation:** Locates specific tables inside a Google Doc template, dynamically appends new rows preserving the original formatting, and automatically cleans up the initial placeholder rows.
- **🧹 Data Sanitization:** Cleans and formats strings and numbers (e.g., standardizing decimal separators, removing extra spaces) before inserting them into the final document.
- **📁 Automated Organization:** Saves the newly generated document directly into a designated Google Drive folder.

## 🚀 Setup & Installation

1. Open your Google Sheet containing the Master Data.
2. Navigate to **Extensions > Apps Script** in the top menu.
3. Delete any existing code in the editor and paste the contents of `generador_listados.js`.
4. Update the **Configuration Variables** at the top of the script (see below).
5. Click the **Save** icon.
6. Run the `generadorListadosEspecialidad` function. Grant the necessary permissions to Google Apps Script the first time you execute it.

## ⚙️ Configuration

Before running the script, make sure to update the following placeholder variables at the top of the code with your actual Google Drive/Sheets IDs:

```javascript
const ID_PLANTILLA_LISTADO = 'YOUR_TEMPLATE_DOC_ID_HERE'; // The ID of your Google Doc template
const ID_BASE_NOTAS_LISTADO = 'YOUR_SPREADSHEET_ID_HERE'; // The ID of the external data spreadsheet
const ID_CARPETA_DESTINO_LISTADO = 'YOUR_DRIVE_FOLDER_ID_HERE'; // The ID of the destination folder
