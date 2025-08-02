JPD Call Centre and COVID-19 Dashboard Project
Overview
This project is a comprehensive dashboard designed to analyze and visualize two distinct datasets: JPD Call Centre performance metrics from July to December 2017 and COVID-19 worldwide case and death data for the first quarter of 2020. The dashboard provides insights into call center operations and the early global spread of COVID-19, offering a dual-purpose tool for operational analysis and epidemiological tracking.
The project leverages data from an Excel file (covid_19_2020.xlsx) containing multiple sheets with structured data. It is designed to be a reusable and extensible framework for visualizing call center KPIs and public health data, suitable for operational managers, analysts, and researchers.
Project Objectives

Call Centre Analysis: Monitor and evaluate key performance indicators (KPIs) such as Average Speed of Answer (ASA), Resolution Rate (RR), Service Level (SL), and Abandon Rate (AR) for the JPD Call Centre from July to December 2017.
COVID-19 Tracking: Visualize the geographic and temporal distribution of COVID-19 cases and deaths worldwide in Q1 2020, including regional breakdowns and country-specific data.
Actionable Insights: Provide clear, data-driven insights to improve call center efficiency and understand early COVID-19 trends.
Interactive Visualizations: Enable users to explore data through dynamic charts and maps for both datasets.

Data Description
The project uses the covid_19_2020.xlsx file, which contains the following sheets:
1. Dashb (JPD Call Centre Analysis)

Purpose: Summarizes call center performance metrics for July to December 2017.
Key Metrics:
Total Calls: 7,730 monthly average.
Average Speed of Answer (ASA): 55.15 seconds (target: 35 seconds).
Resolution Rate (RR): 77.93% (target: 65%, achieved).
Service Level (SL): 71.72% (target: 80%, not achieved).
Abandon Rate (AR): 8.95% (target: 10%, achieved).


Agent Data: Tracks individual agent performance (e.g., Adams, Berkhart) across days.
Time Period: July 2017 (Excel date: 42917) to December 2017.

2. Data (Call Data)

Purpose: Detailed call logs for the JPD Call Centre.
Columns:
Call ID, Call Date, Customer ID, Priority, Query Type, IVR/Queue/Agent Timestamps, Agent Name, Satisfaction (1-5), Resolved (Yes/No), Month, Year.


Key Insights:
Contains 46,632 call records.
Tracks call handling times (IVR, Queue, Agent) and customer satisfaction.
Agents include Stevens, Adams, Berkhart, Katz, and others.


Data Notes: Some records have missing Customer IDs or invalid entries (e.g., "#NAME?").

3. COVID-19 Daily Cases

Purpose: Tracks daily new and cumulative COVID-19 cases by region in Q1 2020.
Columns: Date Reported, Americas, Africa, Asia, Europe, Oceania, Worldwide New Cases, Cumulative Cases.
Key Insights:
Data spans January 1, 2020 (Excel date: 43831) to March 31, 2020 (Excel date: 43921).
Cumulative cases reach 688,829 by March 31, 2020.
Significant spikes in cases, e.g., 59,300 new cases on March 26, 2020.


Source: European Centre for Disease Prevention and Control (ECDC).

4. COVID-19 Deaths

Purpose: Records daily deaths in China, Italy, and the USA, with death rate and demographic breakdowns.
Columns: Date, China, Italy, USA, Death Rate, Gender/Age Breakdowns.
Key Insights:
Deaths increase significantly in March 2020, especially in Italy (e.g., 971 deaths on March 27, 2020).
Demographic data shows higher death rates for males (2.8%) and those aged 70+ (22.8%).


Data Notes: Limited to three countries; some days have zero deaths.

5. COVID-19 Cases by Country

Purpose: Provides country-level case data with geographic coordinates.
Columns: Country, Geoid, Cases, Latitude, Longitude.
Key Insights:
Covers 203 countries, with the USA (529,951 cases) and Spain (161,852 cases) as the highest by March 31, 2020.
Useful for geospatial visualizations (e.g., maps).


Data Notes: Some countries (e.g., Zimbabwe) appear multiple times, requiring deduplication.

6. Calculations

Purpose: Aggregates call center metrics by month and agent.
Key Metrics:
Monthly Calls, Abandon Rate, Queue Time, Service Level, Talk Time.
Agent Satisfaction Ratings (e.g., Ellis: 4.14, Adams: 2.72, target: 3.2).


Data Notes: Contains "#NAME?" errors, indicating potential formula issues.

7. Sheet2 (Agent Time Summary)

Purpose: Summarizes daily agent time (in seconds) for each agent.
Key Insights: Tracks agent activity across specific dates (e.g., Adams: 19,825 seconds on July 1, 2017).
Data Notes: Sparse data for some agents (e.g., Daniels, Ellis) on certain days.

Project Features

Call Centre Dashboard:
Visualizes KPIs (ASA, RR, SL, AR) against targets.
Displays agent performance (satisfaction, resolution rates) over time.
Highlights monthly trends (e.g., September 2017 had the highest service level at 82.59%).


COVID-19 Dashboard:
Plots daily new cases by region (line/bar charts).
Maps country-level cases using latitude/longitude.
Tracks death trends in China, Italy, and the USA.


Data Cleaning:
Handles missing values, invalid entries (e.g., "#NAME?"), and duplicates.
Converts Excel dates (e.g., 42917) to readable formats (e.g., July 1, 2017).


Interactive Visualizations:
Built with Recharts for responsive charts.
Supports filtering by month, region, or agent.



Technical Details

Tech Stack:
Frontend: HTML, JSX, React, Recharts, Tailwind CSS.
Data Processing: JavaScript with PapaParse for CSV parsing.
Dependencies:
prop-types.min.js
react@18.2.0, react-dom@18.2.0
babel-standalone@7.23.2
papaparse@latest
chrono-node@1.3.11
recharts@2.15.0




Data Loading: Uses loadFileData("covid_19_2020.xlsx") to load and parse data at runtime.
Deployment: Single-page HTML application, runnable in any modern browser.

Installation and Setup

Clone the Repository:git clone https://github.com/your-username/jpd-call-centre-covid19-dashboard.git


Install Dependencies:
No local installation required; all dependencies are loaded via CDNs.


Run the Application:
Open index.html in a browser to view the dashboard.
Ensure covid_19_2020.xlsx is accessible for data loading.



Usage

Call Centre Analysis:
View overall KPIs in gauge or bar charts.
Filter by month or agent to analyze performance trends.
Compare actual metrics (e.g., ASA) against targets.


COVID-19 Analysis:
Explore daily case trends by region using line charts.
Visualize country-level cases on a map.
Analyze death rates by country or demographic.


Interactivity:
Hover over charts for detailed tooltips.
Use filters to focus on specific time periods or regions.



Interesting Insights

Call Centre: September 2017 was the best-performing month, with a service level of 82.59% (exceeding the 80% target) and the lowest queue time (31.69 seconds).
COVID-19: The USA saw a dramatic case surge in late March 2020 (529,951 cases by March 31), while Oceania reported minimal cases (e.g., 567 on March 31).
Unexpected Finding: The call center’s lowest satisfaction rating (Adams: 2.72) suggests potential training needs, while Ellis (4.14) consistently exceeded the target of 3.2.

Future Enhancements

Integrate real-time data feeds for ongoing call center metrics.
Expand COVID-19 data to include later quarters of 2020.
Add predictive analytics for call volume or case trends.
Enhance interactivity with drill-down capabilities for specific agents or countries.

Contributing
Contributions are welcome! Please:

Fork the repository.
Create a feature branch (git checkout -b feature/new-feature).
Commit changes (git commit -m "Add new feature").
Push to the branch (git push origin feature/new-feature).
Open a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For questions or feedback, please contact your-email@example.com or open an issue on GitHub.
