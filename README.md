# Redbus Data Scraping with Selenium & Dynamic Filtering using Streamlit

## Table of Contents

- [Project Overview](#project-overview)
- [Skills Gained](#skills-gained)
- [Domain](#domain)
- [Problem Statement](#problem-statement)
- [Business Use Cases](#business-use-cases)
- [Approach](#approach)
  - [Data Scraping](#data-scraping)
  - [Data Storage](#data-storage)
  - [Streamlit Application](#streamlit-application)
- [Results](#results)
- [Evaluation Metrics](#evaluation-metrics)
- [Technical Stack](#technical-stack)
- [Dataset Details](#dataset-details)
- [Database Schema](#database-schema)
- [Installation and Setup](#installation-and-setup)
- [Usage](#usage)
- [Project Deliverables](#project-deliverables)
- [Coding Standards & Version Control](#coding-standards--version-control)
- [License](#license)

## Project Overview

The **Redbus Data Scraping with Selenium & Dynamic Filtering using Streamlit** project automates the collection and visualization of bus travel data from Redbus, providing a user-friendly interface to filter and analyze routes, schedules, pricing, and seat availability.

## Skills Gained

- Web Scraping using Selenium
- Python scripting
- Streamlit application development
- SQL database design and interaction
- Data analysis and filtering

## Domain

Transportation

## Problem Statement

The *Redbus Data Scraping and Filtering with Streamlit Application* aims to revolutionize the transportation industry by providing a comprehensive solution for collecting, analyzing, and visualizing bus travel data. By automating data extraction from Redbus and offering powerful filtering capabilities, this tool enhances operational efficiency and strategic planning.

## Business Use Cases

- **Travel Aggregators**: Real-time bus schedules and seat availability for customers.  
- **Market Analysis**: Travel pattern analysis for market research.  
- **Customer Service**: Customized travel options based on user preferences.  
- **Competitor Analysis**: Pricing and service-level comparison with competitors.  

## Approach

### Data Scraping

- Use Selenium to automate extraction of:
  - Routes
  - Schedules
  - Prices
  - Seat availability

### Data Storage

- Store scraped data in a SQL database for structured querying and analysis.

### Streamlit Application

- Develop an interactive Streamlit app to display and filter data.  
- Implement filters for:
  - Bus type (Sleeper / Seater / AC / Non-AC)
  - Route
  - Price range
  - Star rating
  - Availability

## Results

- Successfully scraped data for a minimum of 10 Government State Bus Transport services and selected private operators.  
- Structured SQL database populated with bus details.  
- Interactive and efficient Streamlit application for data filtering.

## Evaluation Metrics

- **Data Scraping Accuracy**: Completeness and correctness of scraped data.  
- **Database Design**: Efficiency and normalization of schema.  
- **Application Usability**: User experience and performance.  
- **Filter Functionality**: Responsiveness and accuracy of filters.  
- **Code Quality**: Adherence to PEP 8, modularity, and documentation.

## Technical Stack

- **Languages**: Python  
- **Libraries**: Selenium, SQLAlchemy (or sqlite3), Streamlit, pandas  
- **Database**: MySQL (or SQLite)  
- **Tools**: Git, GitHub  

## Dataset Details

Data is sourced from [Redbus](https://www.redbus.in/). Fields include:

- **route_name**: Start and end locations.  
- **route_link**: URL for route details.  
- **busname**: Operator name.  
- **bustype**: Sleeper / Seater / AC / Non-AC.  
- **departing_time**: Scheduled departure.  
- **duration**: Journey time.  
- **reaching_time**: Arrival time.  
- **star_rating**: Passenger rating.  
- **price**: Ticket cost.  
- **seats_available**: Current availability.

## Database Schema

**Table:** `bus_routes`

| Column           | Data Type | Description                    |
| ---------------- | --------- | ------------------------------ |
| id               | INT       | Primary key (auto-increment)   |
| route_name       | TEXT      | Bus route (origin-destination) |
| route_link       | TEXT      | URL to route details           |
| busname          | TEXT      | Bus operator name              |
| bustype          | TEXT      | Type: Sleeper/Seater/AC/Non-AC |
| departing_time   | TIME      | Departure time                 |
| duration         | TEXT      | Journey duration               |
| reaching_time    | TIME      | Arrival time                   |
| star_rating      | FLOAT     | Service rating                 |
| price            | DECIMAL   | Ticket price                   |
| seats_available  | INT       | Seats available                |

SQL to create table:

```sql
CREATE TABLE bus_routes (
    id INT AUTO_INCREMENT PRIMARY KEY,
    route_name TEXT,
    route_link TEXT,
    busname TEXT,
    bustype TEXT,
    departing_time TIME,
    duration TEXT,
    reaching_time TIME,
    star_rating FLOAT,
    price DECIMAL(10,2),
    seats_available INT
);