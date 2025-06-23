Markdown

# [Market Expansion Data Study]

---

## Table of Contents

- [1. Introduction](#1-introduction)
- [2. Features](#2-features)
- [3. Getting Started](#3-getting-started)
    - [3.1. Prerequisites](#31-prerequisites)
    - [3.2. Installation](#32-installation)
- [4. Usage](#4-usage)
  - [4.1. Database Setup](#41-database-setup)
  - [4.2. SQL Analysis](#42-sql-analysis)
  - [4.3. Data Visualization (Tableau)](#43-data-visualization-tableau)
  - [4.4. Final Presentation](#44-final-presentation)
- [5. Project Components](#5-project-components)

---

## 1. Introduction

This repository showcases our Market Expansion Data Study, a collaborative project tackling a complex, real-world business challenge to determine if partnering with "Magist" is advisable. As a project team, we used data analysis and strategic thinking to develop a data-driven recommendation. This project highlights our proficiency in SQL for data analysis and our skills in data visualization using Tableau to create plots for our final presentation. 
Our analysis concludes that Magist is unsuitable for our high-end tech products due to their low tech order volume and minimal tech revenue. We recommend seeking an alternative partner. 

For detailed documentation on the case study, companies, schema, business questions, and presentation structure, please refer to the [Miro Board](https://miro.com/app/board/uXjVIGWwBlk=/?moveToWidget=3458764623835036060&cot=14).

---

## 2. Features

- **Real-World Business Challenge**: Deals with a complex and sometimes unclear business situation.
- **SQL Analysis**: Shows how I prepared and analyzed data using SQL to find important information.
- **Tableau Visualizations**: Demonstrates my ability to create effective charts and dashboards for good data communication.
- **Smart Business Choices**: Highlights the team's skill in making good decisions even with incomplete information.
- **Recommendation from Data**: The project ends with a clear suggestion based on our data analysis, research, and visuals.
- **Complete Data Process**: Covers everything from getting data (SQL dump) to analyzing it (SQL queries), visualizing it (Tableau), and sharing the final message (Presentation).

---

## 3. Getting Started

This section guides you on how to set up your environment to review the various components of the Market Expansion Data Study.

### 3.1. Prerequisites

To fully explore this project, you will need the following software:

-  **MySQL**: For setting up and interacting with the magist_dump.sql database.
  - [MySQL Workbench](https://dev.mysql.com/downloads/workbench/) (>= Version 8.0.41)
- **Tableau** Public / Desktop: To view and interact with the Tableau visualization workbook (Magist.twbx).
  - [Tableau Public](https://public.tableau.com/app/discover) or [Tableau Desktop](https://www.tableau.com/products/desktop)

### 3.2. Installation

Follow these steps to clone the repository and access the project files:

```bash
# Clone this repository
git clone https://github.com/Cebulva/market-expansion-data-study.git

# Navigate into the cloned repository directory
cd market-expansion-data-study
```

---

### 4. Usage

This project consists of several interconnected components, from database setup and SQL analysis to data visualization and a final presentation. Follow the steps below to explore each part.

### 4.1. Database Setup
The core data for this study is contained in a MySQL database dump. You'll need to download this file and load it into your local MySQL instance.

```bash
# 1. Download the zipped database dump file from Google Drive:
#    Open this link in your browser and download 'magist_dump.sql.zip':
#    https://drive.google.com/file/d/151GL0hwaA0NmVUupNnNQVRzhV0YCCuaH/view?usp=sharing

# 2. Save the downloaded 'magist_dump.sql.zip' file into the 'Data/' folder of your cloned repository.
#    (e.g., market-expansion-data-study/Data/magist_dump.sql.zip)

# Navigate to the directory where you saved the zip file, e.g.:
cd market-expansion-data-study/Data/

# Unzip the file. This will create 'magist_db.sql' in the same directory.
unzip magist_db.sql.zip

# 3. Log in to your MySQL server
mysql -u your_username -p

# 4. Inside the MySQL client, create a new database (e.g., 'magist_db')
CREATE DATABASE IF NOT EXISTS magist_db;

# 5. Select the newly created database
USE magist_db;

# 6. Load the database dump.
#    Since the file is zipped, you need to decompress it and pipe its content directly into MySQL.
#    Ensure you run the command below from the root of your cloned repository
#    (e.g., 'market-expansion-data-study/'), as the zipped dump is in the 'Data/' folder.

#    For .gz files (most common for SQL dumps):
gunzip < Data/magist_dump.sql.gz | mysql -u your_username -p magist_db

#    If the file is a .zip archive (less common for SQL dumps, but possible):
#    unzip -p Data/magist_dump.sql.zip | mysql -u your_username -p magist_db

#    Alternatively, you can first unzip the file and then SOURCE it (less efficient for large files):
#    gunzip Data/magist_dump.sql.gz  # This will create Data/magist_dump.sql and remove the .gz
#    SOURCE Data/magist_dump.sql;

# You can now exit the MySQL client (if you logged in separately)
# exit;
```

### 4.2. SQL Analysis
The SQL queries used for data extraction and analysis are stored in the Code/ directory. These queries formed the basis for insights from the magist_db database.

**View SQL Analysis Code**: Located in the Code/ folder. View [SQL Analysis File](https://github.com/Cebulva/market-expansion-data-study/blob/main/Code/Exploring_Magist.sql)

### 4.3. Data Visualization (Tableau)

Visualizations created for this study are available as a Tableau workbook and a PDF export.

- **Download Tableau Workbook**: [Magist.twbx](https://drive.google.com/file/d/15ZO5cIy_km00jJ3RTTdT2iNBAwfST9YN/view?usp=sharing) (Requires Tableau Public or Desktop to open and interact.)
- **View Plots PDF**: A static export of all created Tableau plots. [MagistPlots.pdf](https://github.com/Cebulva/market-expansion-data-study/blob/main/Tableau/MagistPlots.pdf)
- **Raw Data for Plots**: The CSV files used as data sources for the Tableau plots. [Data Folder with CSVs](https://github.com/Cebulva/market-expansion-data-study/tree/main/Data)

### 4.4. Final Presentation

The final of this study is a presentation summarizing the findings and delivering the final recommendation.

- **View Presentation**: [Google Slides Presentation](https://docs.google.com/presentation/d/1kwiiCyD-UfqA4ABKSzQ96Ii-RYC8u2okvhK28bIOpmE/edit?usp=sharing) (Offers online collaborative editing and a variety of templates.)

---

### 5. Project Components

This section outlines the key analytical components and resources used throughout the Market Expansion Data Study.

<details>
<summary>Database Schema and Data</summary>
<br>
The core of this study relies on the magist_db database. You can review its structure and the raw data by setting it up locally as described in the Database Setup section. The schema provides a blueprint of the database tables and their relationships.
<br>
<a href="https://github.com/Cebulva/market-expansion-data-study/tree/main/Resources">View Database Schema</a>
</details>

<details>
<summary>SQL Analysis Files</summary>
<br>
Explore the SQL queries used to extract, transform, and analyze the data from the magist_db. These queries form the analytical backbone of the study, enabling the identification of key trends and insights.
<br>
<a href="https://github.com/Cebulva/market-expansion-data-study/blob/main/Code/Exploring_Magist.sql">View SQL Analysis Code</a>
</details>

<details>
<summary>Data for Tableau Plots</summary>
<br>
These CSV files are the direct tables extracted from the magist_dump.sql database dump. They serve as the original data sources that were imported into Tableau to build the various charts and graphs, representing the raw data used for visualization.
<br>
<a href="https://github.com/Cebulva/market-expansion-data-study/tree/main/Data">View Original Data Tables (CSVs)</a>
</details>

<details>
<summary>Tableau Visualizations</summary>
<br>
A collection of interactive dashboards and plots created using Tableau. These visuals help present complex data in a clear and strong way, supporting our recommendation.
<br>
<a href="https://github.com/Cebulva/market-expansion-data-study/tree/main/Tableau">View Tableau Plots Folder</a>
<br>
<a href="https://github.com/Cebulva/market-expansion-data-study/blob/main/Tableau/MagistPlots.pdf">View Plots PDF</a>
</details>

<details>
<summary>Final Recommendation Presentation</summary>
<br>
The presentation showing the project's scope, methodology, key findings, and the final recommendation regarding the Magist deal. This deliverable aims to come with a clear story and actionable insights.
<br>
<a href="https://docs.google.com/presentation/d/1kwiiCyD-UfqA4ABKSzQ96Ii-RYC8u2okvhK28bIOpmE/edit?usp=sharing">View Presentation</a>
</details>
