### 📊 Measures Used in the Project

| Measure Name               | Measure Function (What it Does)                                             | DAX Formula                                                                 |
|----------------------------|-----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| Avg Resolution Time (Hours)| Calculates the average time taken to resolve a crime case in hours         | `Avg Resolution Time (Hours) = AVERAGE(crime_data[Resolution Time (Hours)])` |
| Total Crimes               | Counts the total number of crime records reported in the dataset           | `Total Crimes = COUNTROWS(crime_data)`                                      |
