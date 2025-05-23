# 🛠️ PySpark ETL Pipeline – Enterprise-Scale Log Processing

This project simulates a real-world **data engineering pipeline** using PySpark. It processes 100,000+ nested JSON logs into flattened, partitioned Parquet files — followed by **SQL-based analytics and indexing simulation**.

> 📌 Built to match job roles like **Data Engineer** or **Software Engineer III** in data-heavy environments (e.g. JPMorgan Chase).

---

## 🚀 Features

- ✅ Ingests large-scale nested JSON log data
- ✅ Flattens complex structures (nested fields, arrays)
- ✅ Writes partitioned Parquet files (`event_type`)
- ✅ Simulates analytics with PySpark SQL
- ✅ Simulates indexing with multi-column aggregation

---

## 📂 Folder Structure

```
pyspark-etl/
├── data/
│   └── large_input_logs.json      # 100,000 synthetic logs
├── output/                        # Parquet files (created after ETL)
├── src/
│   ├── etl.py                     # Main pipeline logic
│   ├── transformer.py            # Flattens nested JSON
│   └── writer.py                 # Writes partitioned parquet
├── main.py                        # Entry point to run ETL
├── simulate_sql.py               # SQL & indexing simulation
├── requirements.txt              # Python dependencies
└── README.md                     # You’re reading it!
```

---

## 🧪 Input Sample

```json
{
  "event_id": "abc123",
  "timestamp": "2025-05-01T10:15:00",
  "user": {
    "id": "user001",
    "location": "New York"
  },
  "event_type": "login",
  "details": {
    "ip": "192.168.0.1",
    "device": "mobile"
  }
}
```

---

## ⚙️ How to Run

### 1. Install Dependencies

> You can use GitHub Codespaces or a local Python 3.10+ environment.

```bash
pip install -r requirements.txt
```

### 2. Run the ETL Pipeline

```bash
python main.py
```

This will:
- Load `data/large_input_logs.json`
- Flatten nested fields
- Write partitioned Parquet files to `output/`

### 3. Run SQL Analytics & Index Simulation

```bash
python simulate_sql.py
```

This will:
- Query Parquet files using Spark SQL
- Output event/device analytics & simulated index queries

---

## 📊 Sample SQL Output

```text
+-------------+-------+
|device       |count  |
+-------------+-------+
|mobile       | 40212 |
|desktop      | 30014 |
|tablet       | 29774 |
+-------------+-------+

+----------+-------------+-------+
|event_type|device       |count  |
+----------+-------------+-------+
|login     |mobile       | 10045 |
|purchase  |desktop      | 10112 |
...
```

---

## 🔍 Why This Project?

✅ Designed for roles requiring:
- Data wrangling at scale
- PySpark transformations
- SQL-based analysis
- Scalable file formats (Parquet)
- Interview-readiness for real use cases

---

## 📧 Contact

Built by a transitioning **SAP Basis Engineer** learning **Data Engineering**.  
Feel free to connect for project collaboration or hiring:

- 💼 GitHub: [your-username]
- 📧 Email: [your-email@example.com]
