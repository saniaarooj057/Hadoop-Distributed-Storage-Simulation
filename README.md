# Distributed File Storage Simulation using Hadoop 🐘

## 📌 Project Overview
This project simulates a **Distributed File Storage System** using a Single-Node Pseudo-Distributed Hadoop Cluster. The goal was to demonstrate how Big Data systems store, replicate, and process data using the **MapReduce** programming model.

## 🛠️ Technologies Used
* **Platform:** Ubuntu (WSL) on Windows
* **Software:** Apache Hadoop 3.3.6
* **Language:** Python 3 (for MapReduce)
* **Environment:** Pseudo-Distributed Mode (Single-Node Cluster)

## 📋 Project Breakdown
| Phase | Task | Status |
| :--- | :--- | :--- |
| **Phase 1** | Environment Setup (WSL, Java, SSH) | ✅ Completed |
| **Phase 2** | Hadoop Installation & Configuration | ✅ Completed |
| **Phase 3** | HDFS Initialization & Formatting | ✅ Completed |
| **Phase 4** | MapReduce Job Execution | ✅ Completed |
| **Phase 5** | Replication Testing (Factor = 1) | ✅ Verified |

## 📂 Files in this Repository
* **`mapper.py`**: The Python script that reads data and filters words.
* **`reducer.py`**: The Python script that counts and aggregates the words.
* **`dataset.txt`**: The input text file uploaded to the distributed storage.
* **`output_screenshot.png`**: Proof of the successful MapReduce job execution.

## 🚀 How to Run the Simulation

### 1. Start the Hadoop Cluster
```bash
start-dfs.shUpload Data to Distributed Storage
We create a directory in HDFS and upload our dataset.

Bash

hdfs dfs -mkdir -p /user/sania/project_input
hdfs dfs -put dataset.txt /user/sania/project_inputRun the MapReduce Job
This command sends the Python scripts to the cluster to process the data.

Bash

mapred streaming \
-input /user/sania/project_input/dataset.txt \
-output /user/sania/project_output \
-mapper mapper.py \
-reducer reducer.py
4. View Results
Read the final output from the distributed file system.

Bash

hdfs dfs -cat /user/sania/project_output/part-00000
 Results
(See output_screenshot.png for visual proof) The system successfully processed the dataset, filtering irrelevant terms and counting key terms, proving the functionality of the distributed storage simulation.


### **Step 3: Save Your Changes**
1.  Scroll down to the bottom of the page.
2.  You will see a box that says **"Commit changes"**.
3.  Click the green **Commit changes** button.

### **The Result**
Go back to your main repository page. You will now see a beautiful, formatted report right on the front page with tables, code blocks, and emojis. **It will look like a professional engineer's project.**

**Would you like me to help you double-check the link before you send it to your prof
