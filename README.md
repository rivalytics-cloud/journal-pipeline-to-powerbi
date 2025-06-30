# Journal Mood Pipeline – PySpark + Power BI

This project shows how I took raw journal data from the Clarity CBT Thought Diary app and turned it into a dashboard that tracks my moods, emotions, and patterns over time. I used PySpark to clean and organize the data, then built visuals in Power BI to better understand myself from 2022 to 2024.

---

## 🧾 About the Data

The journal data was exported from the Clarity app as a `.txt` file. Each entry has the following fields:

- `Title` – Name of the journal entry
- `Mood` – The mood I picked (text or numeric)
- `Activities` – List of activities I selected
- `Emotions` – Emotions I felt at the time
- `Details` – The written journal entry (not analyzed)
- `Date` – When the entry was recorded

---

## 🛠️ What I Built

### 1. Cleaned the Data with PySpark
- Loaded the raw `.txt` file into PySpark
- Broke out values from the activity and emotion lists so each one had its own row
- Formatted the dates so I could look at entries by day, month, or year
- Calculated extra info like how long each entry was (word count)

### 2. Exported the Final Dataset
- Saved the cleaned data as a CSV file that could be imported into Power BI

### 3. Built a Power BI Dashboard
- Connected the CSV to Power BI
- Created visuals to help answer specific questions about my journaling habits

---

## 📊 What I Learned From It

These are the questions I wanted to answer once the data was cleaned:

- How did my mood change over time?
- What emotions did I feel the most often?
- Which activities showed up the most when I was feeling good or bad?
- How often did I journal, and which days did I write the most?
- Did I tend to write more when I was in certain moods?

All of this was done without using machine learning or complex text analysis. I focused on organizing the data and setting it up for simple but meaningful insights.

---

## 🧱 Folder Breakdown
journal-mood-pipeline/

│
├── data/

│ ├── clarity_raw.txt # Sample journal export (anonymized)

│ └── processed_journal.csv # Cleaned data for Power BI

│
├── notebooks/

│ └── process_with_pyspark.py # Script to clean and format the data

│
├── visuals/

│ └── journal_dashboard.pbix # Power BI file with the finished dashboard

│
├── requirements.txt

└── README.md
