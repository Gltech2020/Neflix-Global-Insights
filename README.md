# Neflix-Global-Insights
Analysis of Netflix Trends

## Netflix Content Analysis Dashboard

### Dashboard Link: [PowerBI Report] (https://drive.google.com/file/d/1wLnm7qt9eq-y8LGcXplxODPaltBkKl_h/view?usp=sharing)

## Problem Statement
This dashboard analyzes Netflix's global content library to uncover trends in movies, TV shows, directors, and countries. It helps Netflix (or analysts) understand content distribution, identify gaps in regional offerings, and optimize licensing strategies.

**Key Findings:**  
- 57% of titles are Movies, 43% are TV Shows.  
- Top countries (e.g., US, India) dominate production.  
- Opportunities to diversify director demographics.  


## Steps Followed

1. **Data Loading**:  
   - Imported Netflix dataset (CSV/Excel) into Power BI Desktop.  

2. **Data Cleaning**:  
   - Checked for missing values in key columns (e.g., `country`, `release_year`).  
   - Used Power Query to filter irrelevant entries (e.g., "Not Specified" in director names).  

3. **DAX Measures**:  
   - Created calculated columns for content age groups:  
     ```DAX
     Content Age = 
     IF(
       Netflix[release_year] >= 2020, "New (2020+)",
       IF(
         Netflix[release_year] >= 2010, "Recent (2010-2019)",
         "Classic (Pre-2010)"
       )
     )
     ```
   - Added metrics like `Total Titles`, `% Movies vs. TV Shows`.  

4. **Visualizations**:  
   - **Cards**: Displayed total titles (8,807), movies (6,131), and TV shows (2,676).  
   - **Maps**: Visualized content by country (749 countries).  
   - **Bar Charts**: Compared content types by release year.  
   - **Slicers**: Added filters for `country`, `director`, and `content type`.  

5. **Publishing**:  
   - Published to Power BI Service for sharing.  

---

## Insights

### 1. Content Distribution  
- **Movies**: 6,131 (69.6%)  
- **TV Shows**: 2,676 (30.4%)  
- **Top Countries**: US (30%), India (15%), UK (10%).  

### 2. Director Diversity  
- **Total Directors**: 4,527  
- **Top Directors**: Rajiv Chilaka (22 titles), Raúl Campos (18 titles).  

### 3. Release Trends  
- **Peak Years**: 2018-2020 (highest releases).  
- **Oldest Title**: *Pioneers: First Women Filmmakers* (1925).  

---

## Screenshots

### Power BI Desktop View  
![Desktop View](![Image](https://github.com/user-attachments/assets/a363b3fe-99a0-4e1d-a98a-8bff9909ec81)
---

## Tools Used  
- Power BI Desktop  
- Power Query  
- DAX  

---

## How to Use  
1. Download the `.pbix` file from the repo.  
2. Open in Power BI Desktop.  
3. Interact with slicers to filter data.  

---

**Designed by Gladys Masiiwa**  
*Connect with me on [LinkedIn](https://www.linkedin.com/in/gladys-masiiwa-78bb27a2/)!* Netflix Global Analytics




