# Analysis plan (spreadsheet-friendly)

1. Import the CSV
   - In Excel: Data -> Get & Transform -> From Text/CSV -> Follow import wizard

2. Prepare columns
   - Create Date, Hour, Weekday columns from start_time using Excel datetime functions:
     - Date: =INT([@start_time])
     - Hour: =HOUR([@start_time])
     - Weekday: =TEXT([@start_time],"dddd")

3. Summary statistics
   - Use PivotTable to compute:
     - Count of trips by Date / Weekday / Hour
     - Average trip_duration_minutes by member_type
     - Top 10 stations by trip starts

4. Distribution & outliers
   - Create histograms of trip_duration_minutes
   - Use filters to inspect very long trips (> 120 minutes)

5. Visualizations
   - Line chart for daily trips
   - Column chart for trips by weekday
   - Box plot (or use quartiles) for trip durations by member_type

6. Deliverables
   - A summary sheet with key findings
   - Charts exported as images or kept in Excel workbook
