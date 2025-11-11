# HDFS Practical Assignment – I 

---

## Learning Objectives

By completing this assignment, you will be able to:

1. Perform essential **HDFS file operations**—create, upload, move, copy, and delete.  
2. Understand how **replication** ensures data reliability and what happens when replication cannot reach its target.  
3. Analyze **cluster health and capacity** using HDFS administrative tools.  
4. Interpret **diagnostic reports** and connect them to real-world system performance.  

---

## Part 1 — Core HDFS Operations

---

### Task 1 — Set Up Local and HDFS Directories

**Objective**  
Establish an organized local workspace that mirrors real-world data storage categories before transferring files to HDFS.

**Context**  
Data engineers commonly maintain consistent directory structures between local environments and distributed storage. This practice simplifies data movement, backup, and tracking.

**Steps / Guidelines**
1. Create a main folder for this lab (for example, `hdfs_lab_p1`) in your local file system.  
2. Inside it, design three subfolders:
   - `notes/` — for documentation or small text files  
   - `data/` — for structured numeric or tabular data  
   - `logs/` — for semi-structured application or system logs  
3. Populate each folder with small sample files:  
   - In `notes/` — a short text file describing the purpose of this lab.  
   - In `data/` — a simple dataset such as a sequence of numbers or short CSV table.  
   - In `logs/` — a mock log file containing entries of various log levels (INFO, WARN, ERROR).  
4. Verify that each folder contains at least one valid file and that all are readable.  

**Expected Outcome**  
A well-structured local hierarchy containing sample data ready to upload to HDFS.  

**Deliverable**  
Screenshot of your local directory tree and a short description of each folder’s purpose.  

---

### Task 2 — Upload and Organize Data in HDFS

**Objective**  
Reproduce your local directory structure within HDFS and practice uploading data.

**Context**  
Maintaining parity between local and distributed directories helps in version control and systematic data management across environments.

**Steps / Guidelines**
1. Create equivalent directories inside HDFS for `notes`, `data`, and `logs`.  
2. Upload the prepared files from your local system into their respective HDFS directories.  
3. Verify uploads by listing the contents of each directory.  
4. Compare file names and sizes to confirm consistency between local and HDFS versions.  

**Expected Outcome**  
An identical directory hierarchy inside HDFS with all sample files correctly transferred.  

**Deliverable**  
Screenshot of the HDFS directory structure displaying all folders and files.  

---

### Task 3 — Manage Files in HDFS

**Objective**  
Practice organizing, moving, and validating files within HDFS.

**Context**  
Efficient file management ensures clear data versioning, backup, and archival processes—critical for production systems.

**Steps / Guidelines**
1. Move your log files into an `archive` directory within HDFS to simulate archival of older logs.  
2. Copy one file (for example, a note or dataset) into a `backup` directory to simulate redundancy.  
3. Display the contents of the copied file to confirm that it transferred accurately.  
4. Review the directory structure to confirm that archive and backup directories exist and contain expected files.  

**Expected Outcome**  
Understand safe file reorganization within HDFS while preserving data integrity.  

**Deliverable**  
Screenshot of the final HDFS hierarchy with notes on which files were archived and backed up.  

---

### Task 4 — Clean-Up and Verification

**Objective**  
Reinforce controlled deletion and post-operation validation in HDFS.

**Context**  
Responsible cleanup prevents storage waste while safeguarding essential datasets. This exercise builds habits for production-grade maintenance.

**Steps / Guidelines**
1. Identify one folder (for example, `data`) for removal.  
2. Delete the chosen directory while ensuring that key directories such as `archive` and `backup` remain intact.  
3. Verify that only the selected directory was removed.  
4. Confirm that no critical data was lost in the process.  

**Expected Outcome**  
Safely delete targeted data in HDFS and verify structural integrity afterward.  

**Deliverable**  
Screenshot of the HDFS directory structure after cleanup, noting which directory was deleted.  

---

## Part 2 — HDFS Administration and Diagnostics

---

### Task 5 — Replication Behavior Analysis

**Objective**  
Explore how HDFS replication provides fault tolerance and what occurs when replication targets exceed available DataNodes.

**Context**  
Replication is central to HDFS reliability. Understanding its mechanics is crucial for diagnosing storage warnings and planning capacity.

**Steps / Guidelines**
1. Create a new directory in HDFS specifically for this experiment.  
2. Upload a moderately large file (around 200 MB or more) to ensure block-level distribution.  
3. Observe how many replicas each block has and where they are placed.  
4. Increase the replication factor and recheck the system’s replication status.  
5. Record and interpret any *under-replicated* block messages and relate them to the number of DataNodes in your setup.  

**Expected Outcome**  
Gain insight into how HDFS manages replication and what limits arise in single-node or constrained clusters.  

**Deliverable**  
Screenshot of the replication status and a concise explanation describing the observed replication behavior.  

---

### Task 6 — Cluster Health and Storage Report

**Objective**  
Generate and interpret a detailed HDFS cluster report showing capacity, usage, and DataNode status.

**Context**  
Regular monitoring of cluster health is essential for system reliability and preventive maintenance. This task introduces key diagnostic metrics used by HDFS administrators.

**Steps / Guidelines**
1. Produce a comprehensive HDFS cluster report summarizing capacity, usage, and DataNode details.  
2. Examine critical metrics, such as:  
   - **Configured Capacity** – Total available storage in the cluster.  
   - **DFS Used** – Space currently occupied by files.  
   - **DFS Remaining** – Available free space.  
   - **Under-Replicated Blocks** – Blocks missing full replication.  
   - **Live DataNodes** – Number of active nodes.  
3. Interpret what these metrics indicate about the overall health and performance of your cluster.  
4. Optionally, add or delete a file to see how reported statistics change.  

**Expected Outcome**  
Learn to read and interpret HDFS diagnostic outputs and connect them to real-world cluster behavior.  

**Deliverable**  
Screenshot of the HDFS cluster report and a short explanation of at least three key metrics observed.  

---

## Submission Guidelines

1. Compile all screenshots in sequence and label them clearly by task number.  
2. Ensure explanations are concise and relevant.  
3. Maintain consistent directory names throughout the assignment.  
4. Submit the completed document as a PDF or DOCX file named:  
   `HDFS_Assignment_<number>_<YourName>_<Batch>.pdf`  

---
