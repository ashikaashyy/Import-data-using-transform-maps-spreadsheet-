# Phase 1: Brainstorming & Ideation Phase

**Team ID:** SWTID-2026-2183  
**Project Title:** Import Data Using Transform Maps (Spreadsheet)  
**Phase:** Phase 1 - Brainstorming & Ideation Phase  
**Team Members:** Ashika V (Team Leader & GitHub Repository Owner), Bhavana B A, Athira B S, Nishma W

## Overview
Organisations frequently maintain critical records - such as asset lists, user details, or vendor catalogues - in spreadsheets maintained outside of ServiceNow. Manually re-entering this data into the platform is slow, repetitive, and highly prone to human error, especially when the same records are updated and re-imported over time. During brainstorming, the team explored how ServiceNow's native data import capabilities could be used to bring spreadsheet data into the platform in a controlled, repeatable, and duplicate-free manner.

The team identified that ServiceNow's **Import Set** and **Transform Map** framework is ideally suited to this problem. An Import Set staging table can receive raw spreadsheet data as-is, while a Transform Map can translate that raw data into a proper ServiceNow target table, applying field mapping and coalescing rules along the way. This approach separates "raw incoming data" from "clean platform data," giving the team a safe way to repeatedly re-import updated spreadsheets without creating duplicate records, and to visualise the imported data using reports and dashboards once it lands in ServiceNow.

## Key Idea
Build an end-to-end spreadsheet-to-ServiceNow data pipeline using Import Sets and Transform Maps, with coalesce enabled on a unique field to guarantee that re-importing the same spreadsheet updates existing records instead of duplicating them, and finish with reports/dashboards that make the imported data actionable for stakeholders.
