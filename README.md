# School_District_Analysis
Using Anaconda and Python to analyze standardized scores for a school district.

## Overview 
In this project we developed a report using python and the Pandas library to analyze a school district. We came up with many insights regarding the various schools in the region; including the average test scores per school, average scores by school size, and the budget per student per school. The client was happy with the initial work that we performed, however it later came to their attention that there may have been some academic dishonesty that skewed the results. The client would like us to help solve the problem by removing potentially incorrect scores from the analysis. 

### Purpose
Our objective is to replace the ninth-grade reading and math scores for Thomas High School with NaN values ao that they are not counted. We will then provide a district summary, school summary, and additional data frames for various important metrics.

## Analysis
The first task was to redo our analysis of Thomas High School by removing the ninth graders; which we did this using the loc() method. We then subtracted the ninth graders from the total to get the updated average scores and percentages.

We then used the updated information for Thomas High School to get the district summary, school summary, Top 5 and Bottom 5 schools, average math score by grade, average reading score by grade, and the scores by school spending.

## Results

### From the School Summary
Figure 1: Thomas High School Before Updates
![](./Resources/Fig1_THS_Before.png)
<img src="Resources/Fig1_THS_Before.png" height="100"/>

Figure 2: Thomas High School After Updates
![](/Resources/Fig2_THS_After.png)

Looking at the metrics before and after removing the ninth graders, we can see a few things that changed:
- The average math score decreased by 0.1
- The average reading score increased by 0.1
- The % passing math decreased by 0.1%
- The % passing reading decreased by 0.3%
- The % Overall Passing decreased by 0.3%
- The total school budget and total students (including those excluded from analysis) were unchanged.

### From the District Summary

Figure 3: District Summary Before Updates
![](/Resources/Fig3_DistrictSummary.png)

Figure 4: District Summar After Updates
![](/Resources/Fig4_updated_DistrictSummary.png)

For the district summary, we saw a slightly different impact:
- The average math score decreased by 0.1
- The average reading score was relatively unchanged
- The % passing math decreased by 0.2%
- The % passing reading decreased by 0.1%
- The % Overall Passing decreased by 0.3%
- The total school budget and total students (including those excluded from analysis) were unchanged.

### Additional Topics
- Despite the 0.3% drop in % Overall Passing, Thomas High School remains second in overall performance to Cabrera High School.
- Scores by school spending, school size, and school type appear to have been relative unaffected; even in medium size, medium spending, and charter ranges. 

## Summary
One of the most interesting findings was that the average reading score for Thomas High School increased by 0.1 points, but the % passing reading dropped by 0.3%. A reason for this may have been that the ninth graders may have had more passing grades that were under the average score reading score. The math scores and percentage appear to follow the same path, as well as the overall scores. Although Thomas High School remained in the 2nd spot for overall performance, looking at the scores for other schools shows that it was a close call and that even a 0.3% chorrection in the data can make an impact. It was surprising to see that the scores for school spending, school size, and school type were pretty much unaffected. This might just be becuase of the metrics used, but it may be an indication that the code should be reviewed to see if there were any errors present.
