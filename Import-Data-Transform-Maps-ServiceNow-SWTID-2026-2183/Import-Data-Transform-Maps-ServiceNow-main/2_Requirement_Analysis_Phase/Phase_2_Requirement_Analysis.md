# Phase 2: Requirement Analysis Phase

**Team ID:** SWTID-2026-2183  
**Project Title:** Import Data Using Transform Maps (Spreadsheet)  
**Phase:** Phase 2 - Requirement Analysis Phase  
**Team Members:** Ashika V (Team Leader & GitHub Repository Owner), Bhavana B A, Athira B S, Nishma W

## Problem Statement
Teams that maintain master data in spreadsheets have no simple, repeatable way to bring that data into ServiceNow without manual re-keying. A one-time manual entry does not scale, and re-importing an updated spreadsheet without a de-duplication mechanism risks creating duplicate records in the target table, corrupting reporting and downstream workflows.

## User Story
As a ServiceNow administrator, I want to import spreadsheet data into a staging table and transform it into a target table using a Transform Map, so that records are created or updated automatically, duplicates are avoided through coalescing, and the imported data can be visualised through reports and dashboards for stakeholders.

## Project Objectives
1. Create a spreadsheet-based Data Source and load it into a dedicated Import Set (staging) table.
2. Build a Transform Map with field mappings linking the staging table to the target table.
3. Run the transform, validate that data lands correctly in the target table, and enable coalesce on a unique field to prevent duplicate records on re-import.
4. Create reports and a dashboard so the imported data is visible and actionable to stakeholders.

## Functional Requirements
* Ability to upload an Excel/CSV spreadsheet as a Data Source.
* Auto-generation of an Import Set staging table from the uploaded spreadsheet.
* A Transform Map connecting staging fields to target table fields.
* Coalesce configuration on a unique identifying field (e.g. Employee ID / Asset Tag) to prevent duplicates on repeat imports.
* Reports and a dashboard summarising the imported records.

## Non-Functional Requirements
* The import process must be repeatable without manual cleanup.
* Field mappings must be transparent and easy to maintain.
* The solution must use only out-of-the-box ServiceNow Import Set/Transform Map capabilities (no custom scripting required for the core flow).
