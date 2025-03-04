---
title: projectBCA
description: To distribute bca question  past papers
layout: libdoc/page
layout: libdoc/assets
assets:
    path_from_root: /projectBCA/sqldump
    extensions_enabled:
        - jpg
        - gif
        - zip
        - webp
        - png
order: 2
---
After cloning the [projectBCA](https://github.com/Loftyvirus/projectBCA) repository and setting up the necessary dependencies, follow these steps:  

1. Ensure your backend service has a properly structured `.env` file as follows:  

   ```env
   DB_HOST=localhost
   DB_PORT=3307
   DB_NAME=bca
   DB_USER=
   DB_PASSWORD=
   PORT=3000
   JWT_SECRET=your_random_secret
   ```

2. The backend's running local port will serve as the base URL for the frontend (Vite).  

3. Run both the backend and frontend simultaneously.  

4. Before proceeding, set up MySQL Dump for the initial database structure. Refer to [How to use the MySQL Dump](#how-to-use-the-mysql-dump) for details.  

5. Log in as an admin/supreme user to add papers.  

---

## Adding Question Papers

When adding question papers, follow the format below. The dropdown will auto-generate a default markdown template.

### Default Markdown Template

```markdown
# Pokhara University

**Year**: 2019  
**Semester**: 1  
**Season**: Fall  
**Subject**: Programming Logic and Techniques
```

### How to add the data/questionpapers?

first whenever we select the options from dropdown it will auto genrate a defualt markdown

```markdown
# Pokhara University

**Year**: 2019  
**Semester**: 1  
**Season**: Fall  
**Subject**: Programming Logic and Techniques
```

Now u have to fill up the details in this format like all the paper usually have:

```markdown
---
### 1.
#### (a) Define the evolution of computers. Explain the features of the fourth and fifth generations of computers.
#### (b) What are the functions of a computer? Explain the functional units of a computer with a diagram.
---

### 2.

#### (a) What is firmware and middleware? Differentiate between static and dynamic RAM.

#### (b) What is a softcopy output device? Differentiate between CRT and LCD monitors.

---

### 3.

#### (a) What is Computer Output Microfilm (COM)? Differentiate between impact and non-impact printers.

#### (b) "Operating System works as a mediator between software and hardware." Explain this statement with the functions of an OS.

---

### 4.

#### (a) Explain the following commands with syntax and function:

- REN
- LABEL
- SCANDISK
- PING

#### (b) What is a power supply? Explain the types of UPS in detail.

---

### 5.

#### (a) Define topologies. Explain different types of topologies with a diagram.

#### (b) What is Rating? Differentiate between SCSI and RAID.

---

### 6.

#### (a) What is backup? How is the backup process implemented in a computer? Explain backup methods.

#### (b) Define GUI and TUI/CUI. Differentiate between warm and cold booting.

---

### 7. Write short notes on any two:

- Ergonomically Designed Devices
- ATX Power Supply
- Power Carrying Factor
```

---

# Project BCA: MySQL Data and Schema Backup

This repository contains a MySQL database dump of the `bca` database, including both data and schema for most tables. The `supreme` table is configured to include only the schema (structure) without data.

---

## Contents of the ZIP Archive

- **`data_schema_mysql.zip`**: Contains the MySQL dump for the `bca` database.
  - All tables include both schema and data.
  - The `supreme` table contains only the schema (no data).

---

## How to Use the MySQL Dump

Follow these steps to import the MySQL dump into your database.

### Prerequisites

Ensure the following are installed:

- MySQL Server (or MariaDB)
- MySQL client tools (`mysqldump`, `mysql` command line)

### Steps to Import

1. **Download the ZIP File**  
   Download `data_schema_mysql.zip` from the releases section.

2. **Extract the ZIP File**  
   Extract the contents to locate the `exportfile.sql` dump file.

3. **Access Your MySQL Database**  
   Connect to your MySQL server using the command line:

   ```bash
   mysql -u root -p
   ```

4. **Create the Database (if not existing)**  
   Create the `bca` database if it doesn’t already exist:

   ```sql
   CREATE DATABASE bca;
   ```

5. **Import the MySQL Dump**  
   Import the SQL dump into the `bca` database:

   ```sql
   USE bca;
   SOURCE /path/to/exportfile.sql;
   ```

6. **Verify the Import**  
   Check that the tables were imported successfully:
   ```sql
   SHOW TABLES;
   ```
   - All tables will include data except for the `supreme` table, which will only have the schema.

---

## Additional Notes

1. **`exportfile.sql`**: The `supreme` table contains only the schema. For adding data to the `supreme` table, use the separate file provided.
2. Ensure the instructions are clear, especially for users new to MySQL or those needing detailed setup guidance.
