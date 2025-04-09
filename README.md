# HR Analytics Dashboard - Atlas Labs

## Overview

Power BI dashboard for HR analytics at Atlas Labs. Key areas: employee demographics, hiring, performance, and attrition. Data is current as of December 31, 2022. The dashboard provides insights into employee trends, satisfaction levels, and attrition patterns, enabling data-driven decision-making for HR.

## Dashboard Overview

The dashboard is structured into four key sections:

*   **Overview:** Provides a high-level snapshot of the workforce, including key metrics like total employees, active employees, inactive employees, and the overall attrition rate.
*   **Demographics:** Explores employee demographics based on various factors, including education level and performance rating categories.
*   **Performance:** Analyzes employee performance, tracking key metrics such as job satisfaction, relationship satisfaction, self-rating, environment satisfaction, work/life balance, and manager rating over time.
*   **Attrition:** Examines attrition trends and patterns, breaking them down by travel frequency, overtime requirement, hire date, department and job role, and tenure.

## Key Features

-   **Employee Metrics:**
    -   Total Employees: 1470
    -   Active Employees: 1233
    -   Inactive Employees: 237
    -   Attrition Rate: 16.1%
-   **Hiring Trends:** Visualized by attribution (Yes/No).
-   **Department Distribution:** Active employees by department and job role (Technology, Sales, HR).
-   **Demographics Analysis:** Includes Education Level and Rating Level, showing the distribution of employees across different education levels (e.g., Bachelor's, Master's) and performance rating categories (e.g., Exceeds Expectations, Meets Expectations).
-   **Performance Tracking (March 14, 2021 - July 7, 2023):**
    -   Job Satisfaction (Very Satisfied, Satisfied, Neutral, Dissatisfied, Very Dissatisfied)
    -   Relationship Satisfaction (Very Satisfied, Satisfied, Neutral, Dissatisfied, Very Dissatisfied)
    -   Self Rating (Above and Beyond, Exceeds Expectation, Meets Expectation, Needs Improvement, Unacceptable)
    -   Environment Satisfaction (Very Satisfied, Satisfied, Neutral, Dissatisfied, Very Dissatisfied)
    -   Work/Life Balance (Very Satisfied, Satisfied, Neutral, Dissatisfied, Very Dissatisfied)
    -   Manager Rating (Above and Beyond, Exceeds Expectation, Meets Expectation, Needs Improvement, Unacceptable)
    Filterable by employee and date. The dashboard displays trends and distributions of these satisfaction and performance metrics.
-   **Attrition Analysis:** Analyzed by:
    -   Travel (Frequent, Some, None)
    -   Overtime (Yes/No)
    -   Hire Date
    -   Department & Role
    -   Tenure

## Data Sources

The dashboard uses several data sources:

-   `DimDate.xlsx`: A date dimension table, used for time-based analysis.
-   `EducationLevel.xlsx`: Provides Education Details.
-   `Employee.xlsx`: Core employee data, including demographics, job role, tenure, and attrition.
-   `PerformanceRating.xlsx`: Contains Performance Score data.
-   `RatingLevel.xlsx`: Contains Employees and Managers Performance Rating.
-   `SatisfiedLevel.xlsx`: Contains Employee Satisfaction data.

## Visualizations
![Screenshot (334)](https://github.com/user-attachments/assets/eee6d5a8-58ba-498d-aa20-6f62be69dddf)
![Screenshot (335)](https://github.com/user-attachments/assets/a09124cb-61d8-440a-a15f-36b8dfc5b60c)
![Screenshot (336)](https://github.com/user-attachments/assets/f371e6ab-c46b-412d-9e1e-8a28094d8826)
![Screenshot (337)](https://github.com/user-attachments/assets/f6493804-5330-4f79-9e31-9e84371a00f7)


The dashboard uses a variety of interactive visualizations to present the data effectively:

-   **KPI cards:** Display key metrics at a glance (e.g., Total Employees, Attrition Rate).
-   **Stacked column charts:** Show hiring trends and attrition patterns over time.
-   **Bar charts:** Compare employee counts across different departments and job roles.
-   **Treemaps:** Visualize the distribution of employees across different categories.
-   **Line and column charts:** Track performance metrics and satisfaction levels over time, and analyze attrition trends based on various factors.

## Data Model Relationships

The data model is designed for efficient and accurate analysis. Key relationships include:

*   **Employee** related to:
    *   **DimDate:** For analyzing data over time.
    *   **EducationLevel:** For analyzing demographics based on education.
    *   **RatingLevel:** For analyzing performance based on a given Rating Level.
    *   **SatisfiedLevel:** For Employee Satisfaction.
    *   **PerformanceRating:** This provides the core link for Performance Analysis based on different factors.

## Usage

1.  Open `HR Analytics in Power BI.pbip` in Power BI Desktop.
2.  Refresh data connections to the CSV files to ensure you're working with the latest data.
3.  Explore the tabs: Overview, Demographics, Performance, and Attrition.
4.  Use filters and slicers within each tab to drill down and gain granular insights. For example, on the Performance tab, filter by department and then by Job Satisfaction to see trends within a specific group.

## License

MIT License.
