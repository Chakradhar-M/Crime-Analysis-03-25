### Data Transformation Steps Summary in Power Query:

1. **Loading Data**:  
   The data is loaded from an Excel file (`crime_data.xlsx`).

   ```powerquery
   = Excel.Workbook(File.Contents("C:\Users\PowerBI\crime_data.xlsx"), null, true)
   ```

2. **Promoting Headers**:  
   The first row of the dataset is promoted to headers, making the column names more readable.

   ```powerquery
   = Table.PromoteHeaders(#"Onyx Data -DataDNA Dataset Chal_Sheet", [PromoteAllScalars=true])
   ```

3. **Transforming Column Types**:  
   The column data types are specified to ensure proper formatting for numerical and text data. 

   ```powerquery
   = Table.TransformColumnTypes(#"Promoted Headers",{{"ANC", type text}, {"LATITUDE", type number}, {"BLOCK", type text}, {"offensegroup", type text}, {"location", type text}, {"sector", type text}, {"YBLOCK", type number}, {"METHOD", type text}, {"CCN", Int64.Type}, {"END_DATE", type text}, {"LONGITUDE", type number}, {"offense-text", type text}, {"NEIGHBORHOOD_CLUSTER", type text}, {"SHIFT", type text}, {"PSA", Int64.Type}, {"CENSUS_TRACT", Int64.Type}, {"WARD", Int64.Type}, {"BID", type text}, {"OCTO_RECORD_ID", type any}, {"DISTRICT", Int64.Type}, {"XBLOCK", type number}, {"YEAR", Int64.Type}, {"REPORT_DATE", type text}, {"ucr-rank", Int64.Type}, {"offensekey", type text}, {"START_DATE", type text}, {"VOTING_PRECINCT", type text}, {"OFFENSE", type text}, {"BLOCK_GROUP", type text}})
   ```

4. **Removing Unnecessary Columns**:  
   Several columns that were not required for analysis were removed to reduce dataset complexity and improve processing speed.

   ```powerquery
   = Table.RemoveColumns(#"Changed Type",{"location", "YBLOCK", "XBLOCK", "YEAR"})
   ```

5. **Converting Date Columns to Datetime**:  
   Columns that represent dates such as "START_DATE", "END_DATE", and "REPORT_DATE" are transformed to the `datetime` type for consistency and better handling in visualizations.

   ```powerquery
   = Table.TransformColumnTypes(#"Removed Columns", {{"END_DATE", type datetime}, {"REPORT_DATE", type datetime}, {"START_DATE", type datetime}}, "en-US")
   ```

6. **Adding Custom Columns**:  
   - **Resolution Time (Hours)**: A new column was created to calculate the duration between the "START_DATE" and "END_DATE" in hours. If either date is missing, the value is set to `null`.

     ```powerquery
     = Table.AddColumn(#"Changed Type with Locale", "Resolution Time (Hours)", each if ([END_DATE] = null or [START_DATE] = null) then null else Duration.TotalHours([END_DATE] - [START_DATE]))
     ```

   - **Resolved Status**: A new column was added to track whether the crime was resolved based on the presence of the "END_DATE". If "END_DATE" is null, the status is marked as "Unresolved", otherwise it is marked as "Resolved".

     ```powerquery
     = Table.AddColumn(#"Changed Type1", "Resolved Status", each if [END_DATE] = null then "Unresolved" else "Resolved")
     ```

7. **Replacing Incorrect Values**:  
   - Several values in the "OFFENSE" column were replaced to standardize crime categories. For example, "theft f/auto" was replaced with "theft/auto", and "assault w/dangerous weapon" was standardized to "assault/dangerous weapon".

     ```powerquery
     = Table.ReplaceValue(#"Removed Columns1","theft f/auto","theft/auto",Replacer.ReplaceText,{"OFFENSE"})
     = Table.ReplaceValue(#"Replaced Value","assault w/dangerous weapon","assault/dangerous weapon",Replacer.ReplaceText,{"OFFENSE"})
     ```

8. **Filtering Data**:  
   - The dataset was filtered to retain only crimes from the year 2025, focusing on the most recent data.
   
     ```powerquery
     = Table.SelectRows(#"Inserted Year", each ([Year] = 2025))
     ```

9. **Removing Extra Columns**:  
   Additional columns like "ANC", "CENSUS_TRACT", "WARD", and "VOTING_PRECINCT" were removed from the dataset as they were deemed unnecessary for the analysis.

     ```powerquery
     = Table.RemoveColumns(#"Filtered Rows",{"ANC", "CENSUS_TRACT", "WARD", "VOTING_PRECINCT"})
     ```

---

After applying all these transformations, the dataset was clean and structured for analysis, with columns like `Resolution Time (Hours)`, `Resolved Status`, `OFFENSE`, `SHIFT`, and other key crime attributes ready to be visualized in Power BI.
