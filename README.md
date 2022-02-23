# School District Analysis


*Note: This repository was generated to fulfill assignments (Module 4 Exercises and Challenge) for the UC Berkeley Data Analytics and Visualization Bootcamp. The analysis, content, and format of this report were based on the grading rubric. 

Module exrecises as demonstrated in notebooks jupyter_practics.ipynb, pandas_practice.ipynb, functions_practice.ipynb, cleaning_data.ipynb, cleaning_student_names.ipynb, and PyCitySchools.ipynb include:


The report below is based on code and analyses from PyCitySchools.ipynb and PyCitySchools_Challenge.ipynb.*


## Overview

This report compares analyses of school performance with and without a subset of data removed (specifically Thomas High School 9th graders).

**Data Sources (provided as part of course materials):**
- students_complete.csv
- schools_complete.csv


### Purpose:

We previously performed an analysis of school preformance for all schools within the district for our end client, the school board. Since then, the client has been made aware of possible academic dishonesty and suspect corruption of one of the input data files (students_complete.csv). To uphold standards, the school board has requested a reanalysis of school performance without the suspected tampered data (math and reading scores for Thomas High School 9th graders). This report presents the new analysis and compares summary results against the previous analysis.


---

## Results

### Previous scores for Thomas High Schcool

In our previous analysis, Thomas High School ranked fairly high overall for math, reading, and overall passing scores. While data for Thomas High School 9th graders are reported to be suspect, initial review of math and reading scores across all grades at Thomas High did not reveal any outwardly obvious faults with the 9th grade scores. Both math and reading scores were fairly on par with 10th, 11th, and 12th  grade scores. Standard deviations for math and reading scores were 0.19 and 0.27 respectively (Tables 1 and 2). These were neither outliers or the lowest standard deviations.

**Table 1: Math Scores by School and Grade with Mean and SD**

![math_by_grade_mean_sd.png](/Images/math_by_grade_mean_sd.png)

**Table 2: Reading Scores by School and Grade with Mean and SD**

![reading_by_grade_mean_sd.png](/Images/reading_by_grade_mean_sd.png)



### District Summary Comparison

We repeated our previous analysis after removing reading and math scores for 9th graders at Thomas High School. 

The overall summary for the district was not significantly changed. The average math score for the district dropped by 0.1 point. The reading score average remained the same as well as the percentages of students passing math, reading, and overall (Tables 3 and 4).

**Table 3: District Summary from Previous Analysis**

![district_summary.png](/Images/district_summary.png)

**Table 4: New District Analysis**

![New_district_summary.png](/Images/New_district_summary.png)



### School Summaries Comparison

As with the district summary results, removing 9th grade scores did not significantly impact the overall metrics for Thomas High School (Tables 5 and 6). Average math and reading scores for the school overall changed by less than 1 point, while the percentage of students passing math, reading, or overall decreased by less than 0.3%. 

Across the district, there does appear to be a bimodal distribution for the percentage of overall passing students. Roughly half of the districts' schools had a 90% overall passing rate while half had overall passing rates below 55% (Table 5).

**Table 5: Summary of School Metrics and Scores**

![per_school_summary.png](/Images/per_school_summary.png)


**Table 6: New Summary of School Metrics and Scores**

![New_per_school_summary.png](/Images/New_per_school_summary.png)



### School Rankings Were Not Affected

With our re-analysis, Thomas High School remained the second highest ranking school in the district (Tables 7 and 8). The top 5 ranking schools in the district all had an bove 90% overall passing rate. The ranking of the bottom 5 schools remained the same (Tables 9 and 10); these schools had an overall passing rate of about 53%.

**Table 7: Top 5 Ranked Schools from Previous Analysis**

![top5.png](/Images/top5.png)


**Table 8: Top 5 Ranked Schools from Re-Analysis**

![New_top5.png](/Images/New_top5.png)


**Table 9: Bottom 5 Schools from Previous Analysis**

![bottom5.png](/Images/bottom5.png)


**Table 10: Bottom 5 Schools from Re-Analysis**

![New_bottom5.png](/Images/New_bottom5.png)



### Thomas High School Scores

The mean and standard deviation of math and reading scores across the different grades at Thomas High School also remained very similar after removal of the 9th grade scoress (Tables 11 and 12). 

**Table 11: Average Scores by Grade for Schools**

![New_math_by_grade_mean_sd.png](/Images/New_math_by_grade_mean_sd.png)


**Table 12: Re-analysis of Scores by Grade for Schools**

![New_reading_by_grade_mean_sd.png](/Images/New_reading_by_grade_mean_sd.png)



### Comparison of Performance by Spending, Size, and School Type

We noted previously that the school summaries tables (Tables 5 and 6) revealed a seemingly bimodal pattern for the percentage of students passing overall. Thus, the 15 schools in the district were categorized into bins for spending per student, school size, and type of school (district or charter) for further analyses. These bins did reveal some correlations between student performance and these categories. 

Surprisingly, there was a negative correlation between school spending per student and student performance. For all metrics of student performance, schools in the lowest spending bin (less than $585 per student) had the highest math and reading scores and passing percentages while schools in the highest spending bin had the lowest scores (Tables 13 and 14).

**Table 13: Summary of School Performance by Spending Categories from Previous Analysis**

![spending_summary.png](/Images/spending_summary.png)


**Table 14: Summary of School Performance by Spending Categories from Re-Analysis**

![New_spending_summary.png](/Images/New_spending_summary.png)


In terms of school size, large schools (2001 to 5000 students) performed poorly compared to small and medium schools (Tables 15 and 16). The overall passing percentage for large schools was 58% while 90 and 91% of students in small and medium schools passed overall. While not related directly to student scores, it would be interesting to analyze school spending against school size. Tables 13 through 16 indicate that larger schools may be spending more money per student. However, the higher investment did not seem to correlate with better student performance in our analyses so far.

**Table 15: Summary of School Performance by Size Categories from Previous Analysis**

![size_summary.png](/Images/size_summary.png)


**Table 16: Summary of School Performance by Size Categories from Re-Analysis**

![New_size_summary.png](/Images/New_size_summary.png)


Overall, the eight charter schools in the district performed much better than the 7 district schools (Tables 17 and 18).  Ninety percent of students in charter schools passed overall while only 54% of students in district schools passed overall. 

**Table 17: Performance of District versus Charter Schools from Previous Analysis**

![type_summary.png](/Images/type_summary.png)

**Table 18: Performance of District versus Charter Schools from Re-Analysis**

![New_type_summary.png](/Images/New_type_summary.png)



---

## Summary

Overall, our re-analysis did not result in any significant differences in school and district performance data. Summary tables for performance by spending bins, size, and type of school remain unchanged (Tables 13 through 18). There were minor differences in average math and reading schools for Thomas High once the suspect data (9th grade scores) were removed. However, this did not affect the overall in district performance metrics or significantly alter performance metrics for Thomas High School. Average math and reading scores and passing rates for the school as a whole remained very similar. Our analyses cannot confirm or disprove any evidence of cheating or manipulated data. Additional analyses which may be helpful to the school board include examining historical records for Thomas High School. Significant differences in prior years' scores may indicate suspect data manipulation, especially if 9th grade scores were much lower.

We see trends in student performance corresponding with school size, spending, and type. The most prominent differences are between charter schools versus districts schools and larger schools versus small and medium schools. Charter schools and schools with less then 2000 students outperformed schools in the other categories.

