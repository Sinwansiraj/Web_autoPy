# 🚌 Redbus Data Scraping and Filtering with Streamlit Application

---

## 📸 Sample Outputs (Optional Section)

![App Preview](app_preview.gif)


## 📌 Problem Statement

This project aims to revolutionize the transportation industry by offering a complete solution for collecting, analyzing, and visualizing Redbus travel data. Leveraging **Selenium** for automation, the system extracts key information such as bus routes, schedules, seat availability, prices, and ratings directly from [Redbus](https://www.redbus.in/). The data is stored in a structured **SQL database** and visualized using an **interactive Streamlit application**.

---

## 💼 Business Use Cases

This solution can serve multiple purposes:

- **Travel Aggregators**: Offer customers real-time bus schedules and availability.
- **Market Analysts**: Analyze user preferences and travel trends for research.
- **Customer Experience Teams**: Personalize offerings based on data insights.
- **Competitor Analysis**: Compare service quality and pricing with competitors.

---

## 🔍 Approach

### 1. Data Scraping (Selenium)
- Extract bus details such as route names, types, departure/arrival times, prices, and seat availability from Redbus.

### 2. Data Storage (SQL)
- Store the scraped data into a well-structured SQL database for fast retrieval and querying.

### 3. Streamlit Application
- Build an interactive dashboard to filter and explore bus data using:
  - Bus Type (e.g., Sleeper, Seater)
  - Route Name
  - Price Range
  - Star Rating
  - Seat Availability

---

## 📊 Data Analysis via Streamlit

- Use **SQLAlchemy** to execute queries based on user-selected filters.
- Render dynamic charts or tables in **Streamlit** for better visual exploration.

---

## ✅ Results Expected

- ✅ Scrape data for at least **10 State Government Transport services** and **private buses** for selected routes.
- ✅ Store the dataset in a **SQL database** using a clear and normalized schema.
- ✅ Build a **responsive Streamlit application** with filter functionalities.
- ✅ Ensure intuitive and smooth **user experience**.

---

## 🧪 Project Evaluation Metrics

| Metric                  | Description                                                  |
|------------------------|--------------------------------------------------------------|
| 🔍 Data Accuracy        | Validity and completeness of the scraped data                |
| 🧱 Database Design      | Efficient schema for fast and reliable querying              |
| 🖥 Application Usability| User interface and filter responsiveness                    |
| ⚙️ Code Quality         | Code modularity, documentation, and adherence to PEP 8       |

---

## 🧾 Dataset Information

| Field Name        | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `route_name`      | Origin to destination route description                                     |
| `route_link`      | Link to the specific bus route page on Redbus                              |
| `busname`         | Name of the bus service provider                                            |
| `bustype`         | Bus type (Sleeper/Seater, AC/Non-AC)                                       |
| `departing_time`  | Time when the bus starts the journey                                        |
| `duration`        | Total time of the journey                                                   |
| `reaching_time`   | Expected arrival time                                                       |
| `star_rating`     | Star rating by users                                                        |
| `price`           | Ticket cost                                                                 |
| `seats_available` | Number of available seats at time of scraping                              |

---

## 🛢 Database Schema: `bus_routes`

| Column Name       | Data Type | Description                                      |
|------------------|-----------|--------------------------------------------------|
| `id`              | INT       | Primary Key (Auto-increment)                    |
| `route_name`      | TEXT      | Start to destination route                      |
| `route_link`      | TEXT      | Redbus route link                               |
| `busname`         | TEXT      | Name of the bus operator                        |
| `bustype`         | TEXT      | Type of bus (e.g., Sleeper, Seater)             |
| `departing_time`  | TIME      | Departure time                                  |
| `duration`        | TEXT      | Duration of travel                              |
| `reaching_time`   | TIME      | Arrival time                                    |
| `star_rating`     | FLOAT     | Customer rating                                 |
| `price`           | DECIMAL   | Price of ticket                                 |
| `seats_available` | INT       | Number of vacant seats                          |

---

## 📦 Project Deliverables

- ✅ Python Scripts for:
  - Web Scraping with Selenium
  - SQL Database Creation and Insertion
  - Streamlit App UI and Logic
- ✅ SQL Schema File for database structure
- ✅ Streamlit App Interface with filter controls
- ✅ Documentation of code, usage, and project structure

---

## ⚙️ Technologies Used

- 🐍 Python  
- 🌐 Selenium (Web Automation)  
- 💾 SQL / SQLite / MySQL  
- 🧮 SQLAlchemy  
- 🎛 Streamlit (App Interface)  
- 📊 Data Analysis / Filtering  

---

## 🔄 Version Control & Best Practices

- Git used for version control  
- Follows **PEP 8** coding standards  
- Modular code with functions and docstrings  
- `.env` file excluded using `.gitignore`


---

## 🔗 Useful Links

- 🔗 [Redbus Official Website](https://www.redbus.in/)
- 📚 [Streamlit Documentation](https://docs.streamlit.io/)
- 🧪 [Selenium with Python](https://selenium-python.readthedocs.io/)

---

## 🙌 Contributions

Feel free to fork the repository, raise issues, or submit pull requests to improve this project.
