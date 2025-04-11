<h1 align="center">🔍 Washington D.C. Crime Analysis </h1>

<div style="display: flex; justify-content: space-between; padding: 10px; background-color: #f4f4f4; border-radius: 8px;">
    <h4>📅 Date: March 2025</h4>
    <h4>🛠️ Tools Used: Power BI, Excel, Figma</h4>
    <h4>🏷️ Domain: Public Safety & Urban Analytics</h4>
</div>

--- 

### 📌 Background  

Understanding crime patterns is essential for making cities safer and helping law enforcement and local governments respond more effectively. Urban areas like Washington, D.C. often face complex safety challenges due to high population density, diverse neighborhoods, and varying crime types. With advancements in data collection and analytics, it's now possible to dig deeper into these patterns to support better strategies for crime prevention.

In this project, I analyzed Washington D.C.'s crime data to uncover trends related to crime frequency, location, timing, and severity. The aim was to create a clear, interactive dashboard that helps decision-makers and the community gain useful insights. This reflects my focus on using data not just to present information, but to drive real understanding and action.

---

### 🎯 Objective  

The objective of this project is to design a comprehensive and interactive Power BI dashboard that enables stakeholders to:  
✔️ Identify the most common crimes in each district and neighborhood  
✔️ Understand how crime varies by time of day and location  
✔️ Compare patterns in violent versus property crimes  
✔️ Highlight firearm-related incidents and their distribution  
✔️ Track trends over time to measure progress and pinpoint emerging issues  

This dashboard serves as a powerful decision-support tool for city officials, police departments, and the wider community, helping them take timely and targeted actions to improve public safety.

---


###  📂 Essential Project Links  

| 🧭 Resource | 🔗 Access |
|------------|----------|
| <img src="https://github.com/Chakradhar-M/PBI_Images/blob/main/Portfolio_Icons/database.png?raw=true" width="20" style="vertical-align:middle;"> **Data Source** | 👉 [Click to View Data Source](https://zoomcharts.com/en/microsoft-power-bi-custom-visuals/challenges/onyx-data-march-2025) |
| <img src="https://github.com/Chakradhar-M/PBI_Images/blob/main/Portfolio_Icons/power-bi.png?raw=true" width="22" style="vertical-align:middle;"> **Power BI Live Report** | 📊 [View Interactive Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMWIyY2EyMTgtOTcxMi00NzRmLWE2MzMtOTA5ZWVmZjRjMzI3IiwidCI6IjQ2NTRiNmYxLTBlNDctNDU3OS1hOGExLTAyZmU5ZDk0M2M3YiIsImMiOjl9) |
| <img src="https://github.com/Chakradhar-M/PBI_Images/blob/main/Portfolio_Icons/youtube.png?raw=true" width="20" style="vertical-align:middle;"> **Project Presentation** | 🎬 [Watch Presentation](#) |
| <img src="https://github.com/Chakradhar-M/PBI_Images/blob/main/Portfolio_Icons/linkedin.png?raw=true" width="22" style="vertical-align:middle;"> **LinkedIn Post** | 🔗 [Read on LinkedIn](https://www.linkedin.com/posts/chakradhar-mantena_crime-analysis-dashboard-activity-7310133766541164544-8A8h?utm_source=share&utm_medium=member_desktop&rcm=ACoAAD9y4SkBuDMCUOFBEF1QAO3K3-8MrRRtZZk) |

📌 **Tip:** Right-click or Ctrl + Click to open links in a new tab.


---

### 📊 Sample Raw Data  

<table border="0" cellspacing="1" cellpadding="8">
  <tr>
    <th>ANC</th><th>Latitude</th><th>BLOCK</th><th>offensegroup</th><th>location</th><th>sector</th><th>YBLOCK</th><th>METHOD</th><th>CCN</th><th>END_DATE</th><th>LONGITUDE</th><th>offense-text</th><th>NEIGHBORHOOD_CLUSTER</th><th>SHIFT</th><th>PSA</th><th>CENSUS_TRACT</th><th>WARD</th><th>BID</th><th>OCTO_RECORD_ID</th><th>DISTRICT</th><th>XBLOCK</th><th>YEAR</th><th>REPORT_DATE</th><th>ucr-rank</th><th>offensekey</th><th>START_DATE</th><th>VOTING_PRECINCT</th><th>OFFENSE</th><th>BLOCK_GROUP</th>
  </tr>
  <tr>
    <td>6E</td><td>38.9037316022</td><td>100 - 199&nbsp;block&nbsp;of&nbsp;l&nbsp;street&nbsp;ne</td><td>property</td><td>38.9037316022,-77.0047283051</td><td>5D1</td><td>137319.55</td><td>others</td><td>25002077</td><td>&nbsp;</td><td>-77.0047283051</td><td>theft/other</td><td>cluster 25</td><td>evening</td><td>501</td><td>010603</td><td>6</td><td>noma</td><td>&nbsp;</td><td>5</td><td>399589.87</td><td>2025</td><td>1/4/2025,&nbsp;10:13:33&nbsp;PM</td><td>6</td><td>property|theft/other</td><td>1/4/2025,&nbsp;9:24:00&nbsp;PM</td><td>precinct 144</td><td>theft/other</td><td>010603 3</td>
  </tr>
  <tr>
    <td>2C</td><td>38.9037432394</td><td>18th&nbsp;street&nbsp;nw&nbsp;and&nbsp;l&nbsp;street&nbsp;nw</td><td>property</td><td>38.9037432394,-77.0416730027</td><td>2D3</td><td>137321.65625287</td><td>others</td><td>25008226</td><td>&nbsp;</td><td>-77.0416730027</td><td>theft&nbsp;f/auto</td><td>cluster 6</td><td>midnight</td><td>207</td><td>010700</td><td>2</td><td>golden triangle</td><td>&nbsp;</td><td>2</td><td>396385.3125066</td><td>2025</td><td>1/18/2025,&nbsp;4:03:46&nbsp;AM</td><td>7</td><td>property|theft&nbsp;f/auto</td><td>1/18/2025,&nbsp;3:15:00&nbsp;AM</td><td>precinct 17</td><td>theft&nbsp;f/auto</td><td>010700 1</td>
  </tr>
  <tr>
    <td>1B</td><td>38.917236462</td><td>2000&nbsp;-&nbsp;2099&nbsp;block&nbsp;of&nbsp;8th&nbsp;street&nbsp;nw</td><td>property</td><td>38.917236462,-77.0229457261</td><td>3D2</td><td>138818.94</td><td>others</td><td>25013256</td><td>1/28/2025,&nbsp;12:50:00&nbsp;PM</td><td>-77.0229457261</td><td>theft/other</td><td>cluster 3</td><td>day</td><td>305</td><td>003500</td><td>1</td><td>&nbsp;</td><td>&nbsp;</td><td>3</td><td>398010.08</td><td>2025</td><td>1/28/2025,&nbsp;1:14:31&nbsp;PM</td><td>6</td><td>property|theft/other</td><td>1/28/2025,&nbsp;12:21:00&nbsp;PM</td><td>precinct 37</td><td>theft/other</td><td>003500 3</td>
  </tr>
</table>


---

### 📊 Key Performance Indicators (KPIs)

#### 1️⃣ Total Crimes Reported  
Represents the **total number of crimes** committed within a specific time period. This metric helps in understanding the crime volume and overall safety trends in a given area.  

#### 2️⃣ Time to Resolution (Hours)  
Measures the **average duration** between the occurrence of a crime and its resolution. This includes the time taken for investigation, reporting, and case closure, providing insights into law enforcement efficiency.  

---

## Approach & Methodology
1. **Data Collection** – Gathered data from official crime reports.
2. **Data Cleaning** – Removed inconsistencies, handled missing values.
3. **Exploratory Data Analysis** – Identified patterns, trends, and anomalies.
4. **Visualization** – Used Power BI to create interactive dashboards.
5. **Insights Extraction** – Interpreted findings for law enforcement strategies.

---

## Insights
- Theft and property crimes are the most reported offenses.
- Midnight and evening shifts have the highest crime rates.
- Certain neighborhoods consistently have high crime rates.
- Firearm-related incidents are concentrated in specific districts.

---

## Challenges & Learnings
### **Challenges:**
- Data inconsistencies and missing values required extensive cleaning.
- Identifying crime severity required external ranking references.
- Mapping hotspot analysis accurately took multiple iterations.

### **Learnings:**
- Time-of-day analysis helped in identifying crime patterns.
- Combining multiple datasets enriched the analysis.
- Community policing data can further enhance insights.

---


