## Data Sources

The dashboard uses several data sources. Below are the descriptions of each table (file), including the columns, data types, and descriptions:

*   **FactPerformanceRating.xlsx:** Contains performance review data.

    | Column                     | Data Type | Description                                                                                           |
    | -------------------------- | --------- | ----------------------------------------------------------------------------------------------------- |
    | PerformanceID              | Text      | A unique ID that identifies an individual performance review.                                        |
    | EmployeeID                 | Text      | A unique ID that identifies an employee. Connects to DimEmployee.                                    |
    | ReviewDate                 | Date      | Date an employee’s review took place.                                                                |
    | EnvironmentSatisfaction    | Number    | Rating for employees' satisfaction with their environment. Connects to DimSatisfiedLevel.             |
    | JobSatisfaction            | Number    | Rating for employees' satisfaction with their job role. Connects to DimSatisfiedLevel.                 |
    | RelationshipSatisfaction | Number    | Rating for employees' satisfaction with their relationships at work. Connects to DimSatisfiedLevel.     |
    | WorkLifeBalance            | Number    | Rating for employees' satisfaction with their work-life balance. Connects to DimSatisfiedLevel.       |
    | SelfRating                 | Number    | Rating for employees' performance based on their own view. Connects to DimRatingLevel.                |
    | ManagerRating              | Number    | Rating for employees' performance based on their manager’s view. Connects to DimRatingLevel.         |
    | TrainingOpportunitiesWithinYear | Number    | Number of training opportunities offered in the last 12 months.                                        |
    | TrainingOpportunitiesTaken   | Number    | Number of training opportunities taken.                                                               |

*   **DimSatisfiedLevel.xlsx:** Provides meaning to the satisfaction level.

    | Column          | Data Type | Description                                                                                                                                              |
    | --------------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | SatisfactionID  | Number    | A unique ID that connects to EnvironmentSatisfaction, JobSatisfaction, RelationshipSatisfaction, and Work-Life Balance in FactPerformanceRating.         |
    | SatisfactionLevel | Text      | Provides meaning to the satisfaction level: Very Satisfied, Satisfied, Neutral, Dissatisfied, and Very Dissatisfied. |

*   **DimRatingLevel.xlsx:** Provides meaning to the rating level.

    | Column     | Data Type | Description                                                                                             |
    | ---------- | --------- | ------------------------------------------------------------------------------------------------------- |
    | RatingID   | Number    | A unique ID that connects to SelfRating and ManagerRating in FactPerformanceRating                    |
    | RatingLevel | Text      | Provides meaning to the rating level: Above and Beyond, Exceeds Expectation, Meets Expectation, Needs Improvement, and Unacceptable. |

*   **DimEducationLevel.xlsx:** Provides meaning to the education level.

    | Column          | Data Type | Description                                                                                                          |
    | --------------- | --------- | -------------------------------------------------------------------------------------------------------------------- |
    | EducationLevelID | Number    | A unique ID that connects to Education in DimEmployee.                                                             |
    | EducationLevel | Text      | Provides meaning to the education level: Doctorate, Masters, Bachelors, High School, and No Formal Qualifications. |

*   **DimEmployee.xlsx:** Core employee data.

    | Column                 | Data Type | Description                                                                                                 |
    | ---------------------- | --------- | ----------------------------------------------------------------------------------------------------------- |
    | EmployeeID             | Text      | A unique ID that identifies an employee.                                                                   |
    | FirstName              | Text      | First name of an employee.                                                                                 |
    | LastName               | Text      | Last name of an employee.                                                                                  |
    | Gender                 | Text      | Self-defined employee gender identity.                                                                      |
    | Age                    | Number    | Current age of an employee.                                                                               |
    | BusinessTravel         | Text      | Frequency of business travel - three categories: Frequent Traveller, Some Travel, and No Travel.             |
    | Department             | Text      | Department an employee works in - three categories: Technology, HR, and Sales.                               |
    | DistanceFromHome       | Number    | Kilometer distance between an employee’s home and their office.                                             |
    | State                  | Text      | State where the employee lives.                                                                            |
    | Ethnicity              | Text      | Self-defined employee ethnicity.                                                                              |
    | Education              | Number    | Education level for employees. Connects to DimEducationLevel.                                               |
    | EducationField         | Text      | Employee field of study.                                                                                    |
    | Job Role               | Text      | Current/latest employee job role.                                                                           |
    | MaritalStatus          | Text      | Current/latest employee marital status.                                                                     |
    | Salary                 | Number    | Current/latest employee salary.                                                                               |
    | StockOptionLevel       | Number    | The banding level for stock options that the employee has.                                                   |
    | Overtime               | Text      | Contains "Yes" and "No" to indicate whether an employee is expected to work overtime in their role.          |
    | HireDate               | Date      | Date the employee joined the company.                                                                        |
    | Attrition              | Text      | Contains "Yes" and "No" to indicate whether an employee has left the organization.                           |
    | YearsAtCompany         | Number    | Number of years since the employee joined the organization.                                                  |
    | YearsInMostRecentRole | Number    | Number of years the employee has been in their most recent role.                                             |
    | YearsSinceLastPromotion  | Number    | Number of years since the employee last got promoted.                                                        |
    | YearsWithCurrManager   | Number    | Number of years the employee has been with their current manager                                             |
