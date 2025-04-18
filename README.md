# 🔗 Integrating Azure Cosmos DB with Synapse Link for Analytics

## Overview

In this project, I explored **real-time analytical querying on operational data** by integrating **Azure Cosmos DB** with **Azure Synapse Analytics** using **Synapse Link**. This setup enables seamless, near real-time analytics over NoSQL data without impacting the transactional workload.

## 🧠 What I Did

### 🧾 Cosmos DB Configuration
- Enabled **Azure Synapse Link** in an existing Cosmos DB account
- Created a new **analytical store container** (`Sales`) with autoscaling enabled
- Added sample sales data in JSON format representing customer orders

### 🔗 Synapse Link Integration
- Connected Cosmos DB to **Synapse Studio** using *Connect to external data* > *Azure Cosmos DB for NoSQL*
- Verified the linked database and container in the **Linked tab**

### ⚙️ Interactive Spark Exploration
- Queried Cosmos DB data using a **Spark notebook**  
- Explored nested JSON fields using `df.select()` and PySpark transformations
- Flattened nested objects (`customerdetails`) into structured columns for better usability
- Created a **Spark SQL table** from Cosmos DB and queried it using SQL syntax

### 🧪 Serverless SQL Integration
- Accessed Cosmos DB with **OPENROWSET** via a **serverless SQL pool**
- Created a **credential** using the Cosmos DB primary key to enable access
- Queried the analytical store with a structured schema using JSON path mappings
- Verified **real-time reflection of data updates** in Synapse after inserting a new item in Cosmos DB

## ✅ Key Takeaways

- Cosmos DB + Synapse Link provides **real-time analytics** without ETL
- Spark notebooks can efficiently handle and flatten nested JSON structures
- Serverless SQL pools offer **cost-effective, schema-on-read** querying over Cosmos DB
- This integration supports **hybrid transactional/analytical processing (HTAP)** use cases

---

🔗 **Want to connect or follow more of my journey? Let’s connect on [LinkedIn](https://www.linkedin.com/in/eyilan/)**  
