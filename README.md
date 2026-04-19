# Bright TV: Viewership & Demographic Analysis

## Project Overview
This project focuses on integrating and analysing Bright TV's viewership logs and user profile registry to provide actionable insights for executive decision-making. By combining behavioural data (what people watch) with demographic data (who is watching), the analysis identifies high-value content categories, peak viewing times, and regional audience hotspots across South Africa.

## Data Sources
Viewership Logs (BrightTV_viewership_csv.csv): Transactional data including UserID, Channel2, RecordDate2 (UTC), and Duration 2
User Profiles (Bright_TV_UserProfiles_csv.csv): Demographic information such as Name, Surname, Gender, Age, and Province


## The Approach
1. Project Planning & Design
Before technical execution, the project followed a rigorous planning phase:
Miro: Used for initial project planning and mind mapping. This allowed for the visual structuring of data relationships, identifying potential bottlenecks in null handling, and defining the logic for age and channel categorisation.
Canva: Utilised to develop a Gantt chart, ensuring the project timeline for data cleaning, SQL development, and executive reporting remained on track.
2. Data Integration (Databricks SQL)
The viewership and user profile tables were merged using a LEFT JOIN on the UserID column
. This created a unified dataset linking viewing sessions to specific demographic profiles.
3. Data cleaning & Null Handling
Placeholder Handling: Entries containing the string "None" (prevalent in the name and surname columns) were converted to true NULLs and defaulted to "Unknown"
.
Age Normalisation: Users with an Age of 0 were treated as NULL to ensure accurate demographic calculations
.
4. Feature Engineering
Time Localisation: Per project requirements, UTC timestamps were converted to South African Standard Time (UTC+2).
DayParts: Hours were segmented into Morning, Afternoon, Evening, and Night classes.
Categorisation: Channels were grouped into buckets such as Sports (e.g., ICC Cricket World Cup 2011, SuperSport Blitz), Kids (Cartoon Network, Boomerang), and Entertainment (Trace TV, Africa Magic)
.

## Strategic Insights Derived
Content Drivers: High-impact sporting events like the ICC Cricket World Cup 2011 are major drivers for long-duration viewing sessions
.
Audience Diversity: The platform successfully reaches a broad age range, with confirmed users as young as 9 and as old as 79.
Geographic Hotspots: Concentrated activity is visible in provinces such as Gauteng and Western Cape
.

## Tools Used
Miro: Planning and Mind Mapping.
Canva: Gantt Chart and Project Scheduling.
Databricks SQL: Data Integration, Cleaning, and Analytical Querying.
Microsoft PowerPoint: CEO-level Strategic Reporting.
