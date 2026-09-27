# Phase 6: Project Testing Phase

**Team ID:** SWTID-2026-2183  
**Project Title:** Import Data Using Transform Maps (Spreadsheet)  
**Phase:** Phase 6 - Project Testing Phase  
**Team Members:** Ashika V (Team Leader & GitHub Repository Owner), Bhavana B A, Athira B S, Nishma W

## Testing Execution Steps
1. Navigated to **System Import Sets > Load Data** and uploaded the source spreadsheet to create the Data Source.
2. Ran **Load Data** to generate the Import Set staging table and confirmed the row/column count matched the spreadsheet.
3. Opened the Transform Map and verified all field maps pointed to the correct target fields.
4. Ran **Transform** and checked the target table to confirm records were created with accurate field values.
5. Modified a few rows in the spreadsheet (simulating updates) and a few new rows (simulating new entries), then re-uploaded and re-ran Load Data and Transform.
6. **Validation Success (Coalesce Off):** Confirmed that, prior to enabling coalesce, previously imported records were duplicated on re-import.
7. Enabled Coalesce on the unique field map and repeated the re-import test.
8. **Validation Success (Coalesce On):** Confirmed that existing records were updated in place (no duplicates) while genuinely new rows created new records.
9. Opened the reports and dashboard and confirmed the figures reflected the latest transformed data accurately.

## Testing Evidence
Screenshots of the Data Source/Import Set table, Transform Map field mappings, coalesce configuration, transformed target table records, and the final reports/dashboard are to be captured from the ServiceNow instance and added to this folder as the implementation progresses.
