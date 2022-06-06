# School District Analysis

## Overview of the School District Analysis

The school district analysis consists of preparing standardized test data from a variety of sources and formats for analysis, reporting and presentation to provide insights about performance trends and patterns. The insights are used to inform discussions at the school and district level and assist the school board reagarding school budget and priority. 

The objectives of the original analysis was to analyze data on student funding and students standardized test scores, aggregate the data and showcase trends and school performance.

However, the school board has notified that the students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards. 

Based on this notice, the objective of the following analysis is to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Once the math and reading scores have been replaced. It is expected to repeat the school district analysis that has been initially done and describe how these changes affected the overall analysis. 

---
## School District Analysis Results

The impact of replacing the math and reading scores for Thomas High School with NaNs can be summarize as follows:

### - District Summary Impact

  Comparing the original and updated analysis, it can be seen that there's a neglectable (less than 1%) impact when removing 461 test scores from the    total 39170 student data set.  

  Original Analysis 
![](Images/School_District_Original_Analysis.png)

  Updated Analysis
![](Images/School_District_Updated_Analysis.png)


	
### - School Summary Impact

  The impact of removing the 9th grader scores from the Thomas High School data set is pretty significant with a drop in the overall passing of 26% (from 91% to 65%).
  
  Original Analysis 
![](Images/School_Summary_Original.png)

  Updated Analysis
![](Images/School_Summary_Updated.png)


### - Thomas High School Performance with respect to other schools

  The orginal analysis showed that Thomas High School was second in place with respect to the other schools in terms of performance. However, removing the 9th grader scores from the Thomas High School data set has caused its performance to drop to the 8th place with respect to the other schools.
  
  Original Analysis 
![](Images/THS_Performance_Original.png)

  Updated Analysis
![](Images/THS_Performance_Updated.png)



### - Math and Reading Scores by Grade Impact

  The orginal average scores for math and reading for the 9th grade for Thomas High School was 83.59 and 83.73 respectively, by replacing the scores with NaN, now tables below show no scores for the 9th grade. 
  
  Math Updated by Grade 
![](Images/Math_by_Grade_Updated.png)

  Reading Updated by Grade
![](Images/Reading_by_Grade_Updated.png)


### - Scores by School Spending Impact

  It can be seen in tables below that there's no impact on the scores by school spending when removing 461 test scores from the total 39170 student data set.  

  Original Analysis 
![](Images/Spending_by_School_Original.png)

  Updated Analysis
![](Images/Spending_by_School_Updated.png)

### - Scores by School Size Impact

  It can be seen in tables below that there's no impact on the scores by school size when removing 461 test scores from the total 39170 student data set.  

  Original Analysis 
![](Images/School_Size_Original.png)

  Updated Analysis
![](Images/School_Size_Updated.png)


### - Scores by School Type Impact
 
  It can be seen in tables below that there's no impact on the scores by school type when removing 461 test scores from the total 39170 student data set.  

  Original Analysis 
![](Images/School_Type_Original.png)

  Updated Analysis
![](Images/School_Type_Updated.png)


---
## School District Analysis Summary

The four major changes in the updated school district analysis are: 
* The overall passing from the Thomas High School dropped 26% wih respect to the original analysis.
* The Thomas High school performance dropped from second place to 8th place with repect to the other schools.
* The ninth grades were replaced with NaN therefore there's no average scores for the ninth grade in the updated analysis.
* There is a minimal impact on the district summary as well as on the scores by school spending, size and type.


---
