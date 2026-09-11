# ASG Airlines Data Engineering

## Project Overview

This project is an end-to-end data engineering case study for ASG Airlines. The project focuses on ingesting airline-related data, performing data quality checks, cleaning and transforming the data, handling anomalies, protecting sensitive information, and generating business insights through a Power BI dashboard.

## Objectives

The main objectives of this project are:

- Ingest airline data from source files
- Perform data quality assessment
- Identify missing, duplicate, and invalid records
- Clean and transform the datasets
- Calculate flight duration and identify overnight flights
- Detect anomalous flight records
- Protect sensitive passenger information
- Create analytical datasets and business KPIs
- Develop an interactive Power BI dashboard

## Dataset

The source Excel workbook contains four datasets:

- Flights
- Bookings
- Passengers
- Payments

The datasets are related using flight IDs, booking IDs, and passenger IDs.

## Data Engineering Process

The pipeline follows these major stages:

1. Data ingestion
2. Data quality assessment
3. Data cleaning
4. Data transformation
5. Data validation
6. Anomaly detection
7. PII protection
8. Analytical dataset creation
9. KPI generation
10. Power BI visualization

## Data Quality Checks

The following quality issues were investigated:

- Missing values
- Duplicate records
- Invalid flight IDs
- Invalid booking statuses
- Invalid payment amounts
- Invalid or inconsistent flight durations
- Referential integrity between datasets

## Data Cleaning and Transformation

The data was cleaned by standardizing text fields, removing exact duplicate records, handling missing values, validating identifiers, converting date and time fields, and converting flight durations into numerical minutes and hours.

Flight duration was also recalculated using departure and arrival timestamps. Overnight flights were identified separately.

Invalid flight records were isolated into a rejected dataset instead of being silently removed.

## PII Protection

The source data contains passenger-related sensitive information such as names, email addresses, phone numbers, Aadhaar IDs, passport numbers, and emergency contact information.

Sensitive passenger attributes were protected using hashing where required, and unnecessary sensitive fields were excluded from the final analytical dataset.

Raw source files containing passenger PII should not be uploaded to a public GitHub repository.

## Key KPIs

The project generates KPIs including:

- Total Flights
- Average Flight Duration
- Total Routes
- Total Airlines
- Overnight Flights
- Anomalous Flight IDs
- Route-wise Flight Traffic
- Airline-wise Flight Distribution
- Booking Status Distribution
- Payment Method Distribution

## Power BI Dashboard

The Power BI dashboard provides interactive analysis of airline operations.

The dashboard includes:

- Executive Overview
- Flights by Airline
- Top Routes
- Overnight Flight Analysis
- Booking Status Distribution
- Payment Method Distribution
- Average Flight Duration by Airline
- Source and Destination Airport Analysis
- Flight Duration Distribution

## Project Structure

```text
ASG-Airlines-Data-Engineering/
│
├── data/
│   ├── raw/
│   ├── processed/
│   ├── rejected/
│   └── secure/
│
├── notebooks/
│
├── src/
│
├── output/
│
├── powerbi/
│
├── docs/
│
├── requirements.txt
│
└── README.md
