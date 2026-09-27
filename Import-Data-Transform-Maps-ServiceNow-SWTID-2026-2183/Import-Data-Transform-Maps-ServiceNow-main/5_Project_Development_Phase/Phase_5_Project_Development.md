# Phase 5: Project Development Phase

**Team ID:** SWTID-2026-2183  
**Project Title:** Import Data Using Transform Maps (Spreadsheet)  
**Phase:** Phase 5 - Project Development Phase  
**Team Members:** Ashika V (Team Leader & GitHub Repository Owner), Bhavana B A, Athira B S, Nishma W

## Milestone 1: Creation of Spreadsheet and Table
* Prepared the source spreadsheet with sample records and clearly labelled column headers matching the data to be imported.
* Navigated to **System Import Sets > Load Data** in ServiceNow and created a new Data Source, uploading the prepared spreadsheet (Excel/CSV) as the file.
* Specified the target table name so ServiceNow could auto-generate a staging table to receive the spreadsheet data.
* Confirmed the Data Source record was saved successfully and was ready for the load step.

## Milestone 2: Creation of Import Set Table and Transform Map
* Ran **Load Data** against the Data Source, which generated a new Import Set (staging) table containing all spreadsheet rows and columns.
* Verified the staging table records matched the spreadsheet row-for-row and column-for-column.
* Created a new **Transform Map**, setting the Import Set staging table as the source table and the intended ServiceNow table (e.g. a custom/target table) as the target table.
* Defined **Field Maps** on the Transform Map, mapping each staging column (source field) to the corresponding target table field.

## Milestone 3: Transform Data & Validate and Enable Coalesce to Avoid Duplicate Records
* Executed **Transform** on the Import Set, converting staged rows into records in the target table.
* Opened the target table and validated that each record was created with the correct field values matching the original spreadsheet.
* Re-ran the load and transform with an updated spreadsheet to test for duplicate handling, and observed that without coalescing, duplicate records were created for the same entity.
* Edited the field map for the unique identifying column (e.g. ID/Email/Asset Tag) and enabled the **Coalesce** checkbox on that field map.
* Re-ran the transform and confirmed that matching records were now updated in place instead of being duplicated, while genuinely new rows still created new records.

## Milestone 4: Creation of Reports & Dashboards
* Built a **Report** on the target table to summarise the imported records (e.g. record counts grouped by a key category field).
* Created additional reports to visualise data quality, such as counts of updated vs. newly created records across import runs.
* Assembled the reports into a **Dashboard**, giving stakeholders a single view of the imported data and the health of the import process.
* Verified the dashboard refreshed correctly after subsequent import/transform runs.
