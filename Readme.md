## Link to access the WEB-APP: https://techsolve.streamlit.app/ 


# 💼 Employee Compensation Forecasting Application

An interactive HR analytics tool built as part of a technical case study for TechSolve Inc. This application enables HR and business users to:

* View and filter employee compensation data
* Simulate global or custom compensation increments
* Analyze workforce experience distribution
* Export custom datasets for reporting and analysis

---

## 🛠️ Tools & Technologies Used

| Layer           | Technology             |
| --------------- | ---------------------- |
| Backend         | MySQL                  |
| Frontend        | Streamlit (Python)     |
| Data Processing | Pandas                 |
| Charts          | Plotly                 |
| Other           | Python-dotenv, PyMySQL |

---

## ⚙️ How to Set Up the Project

### 📂 1. Clone the Repository

```bash
git clone https://github.com/anshulraj17/employee-compensation-tool.git
cd employee-compensation-tool
```

### 🧱 2. Set Up the MySQL Database

1. Open your MySQL client (Workbench, DBeaver, CLI)
   * `create a database with name "techsolve_hr"`
2. Run the following in order:
    
   * `sql/create_tables.sql`
   * `sql/insert_roles_locations.sql`
   * `sql/insert_employees.sql`
   * `sql/insert_employee_ratings.sql`
   * `sql/insert_industry_benchmarks.sql`
   * All scripts in `sql/stored_procedures/`

### 🔐 3. Add `.env` File

Create a `.env` file in the root directory:

```
DB_HOST=localhost
DB_USER=yourusername
DB_PASSWORD=yourpassword
DB_NAME=techsolve_hr
```

### 🐍 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 🚀 5. Run the Application

```bash
streamlit run app/main.py
```

---

## ✅ User Stories & Fulfillment

### 🔍 1. Filter and Display Active Employees by Role

* Filter employees by **role**, **location**, and **status** (active/inactive)
* Display a table with: name, role, location, experience, compensation
* Bar chart showing average compensation by location (current vs updated)

➡️ Fulfilled in: `main.py > call_filter_employees()` and main dashboard


![image](https://github.com/user-attachments/assets/a94ed15e-ba12-4299-928a-0c4662b9efbc)



![image](https://github.com/user-attachments/assets/a2de719f-a1d9-4f93-9683-53abe6684ace)

---

### 🧠 2. Group Employees by Years of Experience

* Analyze employee counts by experience bands (e.g., 0–1, 1–2, 3–5 years)
* Optional: filter breakdown by role/location
* Bar chart for easy analysis

➡️ Fulfilled using: filtered data + `value_counts()` logic

![image](https://github.com/user-attachments/assets/310a819e-f5e4-448b-88b5-5bf248210fb2)

![image](https://github.com/user-attachments/assets/8ca89a0e-8b2b-4cbb-a4f7-bc5cb96d5339)

---

### 📈 3. Simulate Compensation Increments

* Input a **global** % increment or
* Apply **custom increments by location** or **per employee**
* View both current and updated compensation
* Visual bar chart comparison (interactive)

➡️ Fulfilled via sidebar logic + `apply()` function on filtered DataFrame
![image](https://github.com/user-attachments/assets/265e4f2c-9638-49b9-9573-08c40ac24e87)



![image](https://github.com/user-attachments/assets/00a8760f-89e1-442e-88ed-4feb6c1cc680)



![image](https://github.com/user-attachments/assets/81f3cd49-0b77-4759-8a3a-167f53fbb462)

![image](https://github.com/user-attachments/assets/a2aff6a1-be5c-44bf-9101-12d7b9d6d31c)


![image](https://github.com/user-attachments/assets/6c9853a7-005e-4501-a0a3-4459609b9f97)

---

### 📁 4. Download Filtered Employee Data

* Download data in CSV format
* Includes filters and updated compensation if simulation applied

➡️ Fulfilled via `st.download_button` using Pandas `.to_csv()`
![image](https://github.com/user-attachments/assets/27a9e40c-dfb2-469e-9244-22a51a610106)



## 📬 Submitted By:

Name - Anshul Mishra
Email - Anshulraj17@gmail.com

---

>  2025 TechSolve Case Study 
