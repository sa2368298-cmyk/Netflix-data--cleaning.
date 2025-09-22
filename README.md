
# Netflix Movies and TV Shows - Cleaned Dataset

## 📌 Project Overview
This project is part of a **Data Analyst Internship Task (Data Cleaning and Preprocessing)**.  
The goal was to clean and prepare a raw dataset containing Netflix Movies and TV Shows by handling missing values, duplicates, inconsistent formats, and standardizing data.

## 🛠️ Tools Used
- **Python (Pandas)** for data cleaning and preprocessing  
- **Jupyter/Colab Notebook** for implementation  

## 🔄 Data Cleaning Steps
1. **Handled Missing Values**
   - Filled missing `director`, `cast`, `country`, and `rating` with `"Unknown"`.
   - Dropped rows where `title` or `type` was missing.

2. **Removed Duplicates**
   - Used `drop_duplicates()` to eliminate duplicate rows.

3. **Standardized Text Values**
   - Converted categorical fields (`type`, `country`, `rating`) to lowercase and stripped spaces.

4. **Converted Date Formats**
   - Changed `date_added` into a standard format (`dd-mm-yyyy`).

5. **Fixed Data Types**
   - Ensured `release_year` is integer type.
   - Standardized `duration` column format (numeric + unit).

## 📊 Cleaned Dataset Preview

| show_id | type     | title            | director          | cast         | country        | date_added | release_year | rating | duration   | listed_in                  |
|---------|----------|------------------|------------------|--------------|----------------|------------|--------------|--------|------------|----------------------------|
| s1      | movie    | the irishman     | martin scorsese  | robert de niro | united states | 27-11-2019 | 2019         | r      | 209 min    | dramas, crime, biography   |
| s2      | tv show  | stranger things  | unknown          | winona ryder  | united states | 15-07-2016 | 2016         | tv-14  | 3 seasons  | sci-fi, horror, drama      |
| s3      | movie    | lagaan           | ashutosh gowariker | aamir khan | india          | 08-04-2001 | 2001         | pg     | 224 min    | dramas, sports             |

## 📌 Summary of Changes
- Filled missing values with `"Unknown"` where applicable.  
- Dropped invalid rows with null critical fields (`title`, `type`).  
- Removed **248 duplicates**.  
- Standardized categorical values to lowercase.  
- Reformatted `date_added` into `dd-mm-yyyy`.  
- Ensured correct data types.  

## 🚀 How to Use
1. Clone this repository.  
2. Load the dataset using Pandas:  

```python
import pandas as pd
df = pd.read_csv("Netflix_Cleaned.csv")
print(df.head())
```

3. Start analyzing or visualizing the data!

---

✅ Cleaned dataset is ready for **analysis or modeling**.  
