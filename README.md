# healthcare-dbms-project
Healthcare DBMS project using Oracle SQL, Python ETL for data cleaning &amp; loading, Flask backend, and a simple frontend UI. Dataset sourced from Kaggle (Healthcare Provider Fraud Detection)

# Healthcare DBMS Project

This project demonstrates how to design and implement a Database Management System (DBMS) using **Oracle SQL**, **Python (ETL + Flask)**, and a simple **frontend UI**.  

The goal is to take raw healthcare data (patients, claims, and hospital records), clean and normalize it, load it into Oracle, and provide a frontend where users can run SQL queries and view results in tabular form.

---

## 📂 Project Structure
healthcare-dbms/
│
├── data/ # raw and cleaned datasets (CSV files, not tracked if large)
├── etl/ # Python scripts for cleaning + loading into Oracle
├── database/ # schema.sql and queries.sql
├── backend/ # Flask backend code
├── frontend/ # frontend (HTML/JS) to query DB
└── README.md


---

## 🚀 Workflow

1. **Dataset Selection**  
   - Dataset sourced from [Kaggle Healthcare Provider Fraud Detection](https://www.kaggle.com/datasets/rohitrox/healthcare-provider-fraud-detection-analysis).  
   - Includes patient demographics and inpatient claim details.  

2. **Data Cleaning (Python)**  
   - Removed duplicates and invalid rows.  
   - Handled missing values (e.g., unknown doctors).  
   - Standardized categorical fields (gender, states).  
   - Converted date fields to standard formats.  

3. **Schema Design (Oracle SQL)**  
   - Normalized into relational tables:
     - `patients`  
     - `claims`  
     - (optional: `diagnoses`, `treatments`, `billing`)  
   - Added primary & foreign keys.  
   - Created indexes for faster queries.  

4. **ETL Process**  
   - Python (`pandas`, `oracledb`) used to load cleaned CSVs into Oracle tables.  
   - Batch inserts with error handling and logging.  

5. **Backend (Flask)**  
   - Exposes REST API endpoints for running safe `SELECT` queries.  
   - Ensures SQL injection protection.  
   - Returns query results as JSON.  

6. **Frontend (HTML/JS)**  
   - Simple UI where users can type SQL queries.  
   - Results displayed in a formatted table.  

---

## 🛠 Tech Stack
- **Database**: Oracle SQL  
- **Backend**: Python (Flask, pandas, oracledb)  
- **Frontend**: HTML, CSS, JavaScript  
- **Version Control**: Git + GitHub  

---

## 📊 Example SQL Queries
- Find total claim reimbursement by state.  
- Get patients diagnosed with diabetes who had > 5 claims.  
- Identify top 5 providers by total reimbursement amount.  
- Count patients by gender and chronic condition.  
- List claims with hospital stays longer than 10 days.  

---

## 📎 References
- Dataset: [Kaggle Healthcare Provider Fraud Detection](https://www.kaggle.com/datasets/rohitrox/healthcare-provider-fraud-detection-analysis)  
- Oracle Database Documentation: [docs.oracle.com](https://docs.oracle.com/en/database/)  

---

## 📌 Next Steps
- Add visualizations (charts for claims & conditions).  
- Extend schema to include outpatient data.  
- Deploy backend & frontend on cloud.  

---

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

