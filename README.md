# Kaggle E-Commerce Analysis with Hadoop & Spark

##  Overview
This project demonstrates the setup of **Hadoop & Spark** on a local machine, loading large datasets into HDFS, and analyzing them using Spark SQL.

**Dataset:** Kaggle E-Commerce (285M rows)

---

##  Tech Stack
- **Hadoop** (HDFS & YARN)
- **Apache Spark**
- **PySpark**
- **Kaggle Dataset**

---

##  Setup Instructions

### 1. Install Dependencies
- Hadoop 3.x
- Spark 3.x
- Python 3.x + PySpark

---

### 2. Starting Hadoop Services
To start Hadoop, run:

```bash
stop-yarn.sh
stop-dfs.sh
start-dfs.sh
start-yarn.sh
```


![Hadoop Services Running](images/start-hadoop-services-jps.png)



### 3. Upload Dataset to HDFS
After extracting the Kaggle dataset, upload it to HDFS:

```bash
# Create directory in HDFS
hdfs dfs -mkdir -p /user/fai/ecommerce/raw

# Upload dataset
hdfs dfs -put data/raw/2019-Nov.csv /user/fai/ecommerce/raw/

# Verify upload
hdfs dfs -ls /user/fai/ecommerce/raw
```

![HDFS Upload](images/hdfs-upload.png)

