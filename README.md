# School-District-Analysis

# Overview of the school district analysis. 

## Purpose
In this project, we are tasked with preparing math and reading assessment scores data for analysis and determine performance trends and patterns by schools, by budget allocations, by grades, by school type and size. These insights will inform discussions and strategic decisions at the school and district levels. Namely, this analysis will asssist the School Board in making decisions on school budgets and priorities. 

Here is the list of deliverables for the analysis of the school district: 

- A high-level snapshot of the district's key metrics, presented in a table format
- An overview of the key metrics for each school, presented in a table format
- Tables presenting each of the following metrics:
    - Top 5 and bottom 5 performing schools, based on the overall passing rate
    - The average math score received by students in each grade level at each school
    - The average reading score received by students in each grade level at each school
    - School performance based on the budget per student
    - School performance based on the school size 
    - School performance based on the type of school
## Additional Information

For this task, we need to be informed about the Family Educational Rights and Privacy Act (FERPA) of 1974, which protects the privacy of student education records. The law applies to all schools that recieve funds under an applciabke program of the US Department of Education. The data needs to be treated with upmost confidentiality. 

Please also note that this analysis was conducted twice due to potential academic dishonesty, which showed possibly altered grades in a specific grade group in a specific school. 

## Resources 

### Dataset
- In the ("schools_complete.csv")[], there are 15 observations and 5 variables corresponding to the School ID, school_name, type, size, and budget columns. This dataset came in cleaned and has no misspellings, case changes, duplicates, or special characters. 
- In the ("students_complete.csv")[], there are 39,170 observations and 7 variables corresponding to the "Student ID", "student_name", "gender", "grade", "school_name", "reading_score", "math_score". Unlike the schools_complete.csv file, this file requires some cleaning to do. For instance, in the student_name column, there is an entry "Dr. Richard Scott".
- The above datasets are merged into one for the analysis. 
- Software: Python 3.7.6 through Jupyter Notebook. 

# Analysis


Since there was a potential academic dishonesty detected for ninth grades at Thomas High School as the grades looked altered, the analysis had to be redone twice. 
[PyCitySchools.ipynb](https://github.com/Aigerim-Zh/School-District-Analysis/blob/main/PyCitySchools.ipynb) shows the analysis including all student data. 
[PyCitySchools_Challenge.ipynb](https://github.com/Aigerim-Zh/School-District-Analysis/blob/main/PyCitySchools_Challenge.ipynb) shows the analysis after omitting possibly altered data. 

## How is the district summary affected?
In the Resources folder of this repository, you can find images for before and after tables. 

After replacing the possibly altered data with NaN values, the metrics did not changed significantly for the whole district:
- The overall passing percentage for the whole district stayed 65% (as a whole number)
- The average math score decreased from 79 to 78.9
- The average reading score stayed 81.9
- % Passing Math stayed 75%
- % Passing Reading stayed 86 

## How is the school summary affected?
The analysis was run for each school. In the second analysis, only 10th to 12th grade data was considered for Thomas High School. 
- The overall passing percentage for Thomas High School for math and reading assessments fell from 90.95% to 90.63%
- The average math score decreased from 83.42 to 83.35
- The average reading score increased from 83.85 to 83.9
- % Passing Math fell from 93.27% to 92.19% 
- % Passing Reading stayed fell from 97.3% to 97.02%



## How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
Despite the changes, Thomas High School remained the second high performing school. 

## How does replacing the ninth-grade scores affect the following:
### Math and reading scores by grade
Scores by school spending
Scores by school size
Scores by school type

Summary: Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.