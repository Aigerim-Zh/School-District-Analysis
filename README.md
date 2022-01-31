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
- In the ["schools_complete.csv"](https://github.com/Aigerim-Zh/School-District-Analysis/blob/main/Resources/schools_complete.csv), there are 15 observations and 5 variables corresponding to the School ID, school_name, type, size, and budget columns. This dataset came in cleaned and has no misspellings, case changes, duplicates, or special characters. 
- In the ["students_complete.csv"](https://github.com/Aigerim-Zh/School-District-Analysis/blob/main/Resources/schools_complete.csv), there are 39,170 observations and 7 variables corresponding to the "Student ID", "student_name", "gender", "grade", "school_name", "reading_score", "math_score". Unlike the schools_complete.csv file, this file requires some cleaning to do. For instance, in the student_name column, there is an entry "Dr. Richard Scott".
- The above datasets are merged into one for the analysis. 
- Software: Python 3.7.6 through Jupyter Notebook. 

# Analysis
Since there was a potential academic dishonesty detected for ninth grades at Thomas High School as the grades looked altered, the analysis had to be redone with replacing the data with missing values. 

[PyCitySchools.ipynb](https://github.com/Aigerim-Zh/School-District-Analysis/blob/main/PyCitySchools.ipynb) shows the analysis including all student data. 
[PyCitySchools_Challenge.ipynb](https://github.com/Aigerim-Zh/School-District-Analysis/blob/main/PyCitySchools_Challenge.ipynb) shows the analysis after omitting possibly altered data. 

In the [Resources](https://github.com/Aigerim-Zh/School-District-Analysis/tree/main/Resources) folder of this repository, you can find the images of summaries before and after the replacement. 

## 1. How is the district summary affected?
**District Summary Before**
![]()

**District Summary After**
![]()
After replacing the possibly altered data with NaN values, the metrics did not changed significantly for the whole district:
- The overall passing percentage for the whole district fell from 65.17% to 64.85%
- The average math score decreased from 78.98 to 78.93
- The average reading score decreased from 81.88 to 81.85
- % Passing Math decreased from 74.98% to 74.76%
- % Passing Reading decreased from 85.8% to 85.66%

## 2. How is the school summary affected?
The analysis was run for each school. In the second analysis, only 10th to 12th grade data was considered for Thomas High School. 
- The overall passing percentage for Thomas High School for math and reading assessments fell from 90.95% to 90.63%
- The average math score decreased from 83.42 to 83.35
- The average reading score increased from 83.85 to 83.9
- % Passing Math fell from 93.27% to 92.19% 
- % Passing Reading fell from 97.3% to 97.02%
**School Summary Before**
![]()

**School Summary After**
![]()
## 3. How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
Despite replacing the ninth grade data, Thomas High School remained the second high performing school. 
**Top Five Schools Before**
![]()

**Top Five Schools After**
![]()
## 4. How are the scores affected by grades?
- The average math and reading scores stayed roughly the same for each grade level before and after. 
**Average Math Score Before**
![]()

**Average Math Score After**
![]()

**Average Reading Score Before**
![]()

**Average Reading Score After**
![]()

## 5. How are the scores affected by school spending?
- The scores also stayed roughly the same by school spending ranges except that for the $630-644 spending range the % Overall Passing decreased from 62.86% to 62.78%. 
- There is a very suprising trend observed, both before and after, of the % Overal Passing decreasing as the spending per student increases. It is obvious, that there are other explanotory factors to higher passing rates. 

**Summary by School Spending Before**
![]()

**Summary by School Spending After**
![]()

## 6. How are the scores affected by school size?
The metrics by school size were slightly affected for **the medium-sized schools**:
- The overall passing percentage for math and reading assessments fell from 90.62% to 90.55%
- The average math score decreased from 83.37 to 83.36
- The average reading score increased from 83.86 to 83.87
- % Passing Math fell from 93.6% to 92.58% 
- % Passing Reading stayed fell from 96.8% to 96.7%
**Summary by School Size Score Before**
![]()

**Summary by School Size After**
![]()
## 7. How are the scores affected by school type?
The only type of school that was slightly affected is the Charter type schools since Thomas High School is a Charter type school. 
**Summary by School Type Score Before**
![]()

**Summary by School Type After**
![]()
# Summary: 
In general, the analysis results were not affected significantly. The small changes that happened included the following:
1. District Summary - all the metrics slightly decreased between 0.1 to 0.5 percentage points.
2. School Summary - all the metrics slightly decreased by less than 1 percentage point except for the average reading score, which incerased by 0.05 value points.
3. Top Five Schools Summary - despite excluding the data for the 9nth graders, Thomas High School remained the second high performing school.
4. Summary by School Spending - the scores stayed roughly the same except that for the $630-644 spending range, in which the % Overall Passing decreased from 62.86% to 62.78%. 
5. Summary by School Size - the metrics stayed relatively the same except for the medium-sized schools, in which the passing percentages fell by less than 0.1 percentage points. 
6. Summary by School Type - as expected, the metrics changed only for Charter schools since Thomas High School is one of them in the data. The passing percentages for the Charter type schools fell by less than 0.1 percentage points. 
