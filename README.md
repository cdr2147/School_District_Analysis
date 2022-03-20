# School_District_Analysis
## Project Overview
Assist the chief data analyst for a city school district who is tasked with preparing, analyzing, and reporting on standardized test data. The goal is to provide insights into data trends at the school and district level and an analysis of student funding and student standardized test scores. The report will be used to help the school board when making decisions regarding school budgets and priorities. 
### Purpose
After performing analysis of provided school data, the school board notifies you that the data in students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth grader. To address this issue, the the chief data analyst requests you to replace the math and reading scores for Thomas High School with NaNs, while keeping the rest of the data intact and to repeat the school district analysis given the update. Below are results after the code has been refactored and how these changes affected the overall analysis.

## Resources
* Data Source: schools_complete.csv, students_complete.csv
* Software: Python 3.7.11

## School District Results
* How is the district summary affected?

After removing Thomas High School 9th grade math and reading scores, 461 less students are counted towards Thomas High School's total students and test averages. This did not impact the distict analysis dramatically given that the data set included 39,000+ students. Metrics decreased slightly, except for the average reading score which was not impacted.

Previous Analysis:
![Old District Analysis](https://user-images.githubusercontent.com/99205688/159177230-d1dbaa10-e3ad-44b2-9a94-588e8b70b574.PNG)

New Analysis:
![New District Analysis](https://user-images.githubusercontent.com/99205688/159177234-59874b17-4922-4cba-8364-27dd5a6fa10a.PNG)

* How is the school summary affected?

When removing the 9th grader and their scores from the data, the school summary for Thomas High School is impacted in that the average math, percentage of passing math, reading and overall percentage passing decreased slightly. The average reading score at Thomas High School increased slightly.

Previous Analysis:
![Old School Summary](https://user-images.githubusercontent.com/99205688/159177598-e0e2fa6f-9de3-46ee-9eed-07e805612883.PNG)

New Analysis:
![New School Summary](https://user-images.githubusercontent.com/99205688/159177602-34d6b20d-6aa6-40b3-bbec-67b389ed075e.PNG)

* How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

If only replacing the 9th graders' math and reading scores with Nans (but not adjusting the total number of students in the score related averages), Thomas High School's overall performance would drop significantly due to lower averages and percentages (about mid-way in school comparison). 
![Nan's ranking](https://user-images.githubusercontent.com/99205688/159177732-4c8cb6e6-1019-4aa2-a085-7e2bce62e872.PNG)

However, with removing the 9th graders entirely from the calculation of student count, Thomas High School still ranked second for highest percentage of overall passing students when compared to other schools, with the percentage overall passing only slightly decreasing due to the replaced scores. The percentage decrease was not enough to impact the ranking as the changes were in the hundreths. 

Previous Analysis:
![Old school ranking](https://user-images.githubusercontent.com/99205688/159177775-4e1b9cec-25f9-499b-8e0d-188f8482ef86.PNG)

New Analysis:
![new school rankning](https://user-images.githubusercontent.com/99205688/159179110-6b21ee93-1c4d-41b4-a11d-48d6aac45cd0.PNG)

Replacing the ninth-grade scores affect on the following:
* Math and reading scores by grade

Math and reading scores by grade were impacted by replacing 9th grade scores with Nans in that the average of scores was no longer calculated and shown as a null value in overall averages. However, given that the changes were hudreths of a decimal point, the overall rounded numbers did not change.

Scores by grade - Math: 

![Math scores by grade](https://user-images.githubusercontent.com/99205688/159178005-eeb2a993-75f6-4316-937c-ff57f059f1cc.PNG)

Scores by grade - Reading:

![reading scores by grade](https://user-images.githubusercontent.com/99205688/159178006-c76265e7-10a1-4424-8255-63c44c37cb08.PNG)

  * Scores by school spending

The scores by school spending decreased slightly for average math score, percentage passing math, reading, and percentage of overall passing for the $631-645 spending range. Average reading scores increased slightly. Given that the changes were hudreths of a decimal point, the overall rounded numbers did not change.

Previous Analysis:

![old spending](https://user-images.githubusercontent.com/99205688/159178018-0786ce92-bfb8-434a-9687-9375da892e65.PNG)

New Analysis:

![new spending](https://user-images.githubusercontent.com/99205688/159178030-c45569f1-6220-4e91-b828-c46830c4570f.PNG)

  * Scores by school size

The scores by school spending decreased slightly for average math score, percentage passing math, reading, and percentage of overall passing for the medium sized schools (1000-1999). Average reading scores increased slightly. Given that the changes were hudreths of a decimal point, the overall rounded numbers did not change.

Previous Analysis:

![old school size](https://user-images.githubusercontent.com/99205688/159178041-37b8023e-374b-40ad-bdb9-042ef324ef6e.PNG)

New Analysis:

![new school size](https://user-images.githubusercontent.com/99205688/159178044-9ee357eb-b746-40d4-a31d-7f1d61837f1f.PNG)

  * Scores by school type
  
The scores by school type were not impacted due to the small change.

Previous Analysis:

![old school type](https://user-images.githubusercontent.com/99205688/159178068-08811bd4-89dc-4521-9abf-e232bf19de3c.PNG)

New Analysis:

 ![new school type](https://user-images.githubusercontent.com/99205688/159178080-5ed66170-5641-4552-927f-741598b138a5.PNG)

 
## School District Summary
In summary, when looking at the data after replacing the 9th grade test scores with Nans, Thomas High School's relative performance decreases quite significantly due to the null test scores being taken into account. The school would drop from the 2nd ranking to the middle ranking of the 15 schools. However, after removing the 9th graders from being counted in the Thomas High School student count, the performance did not change dramatically. Average math scores decreased slightly and average reading scores increased slightly, but changes in performance were within 1% of the original numbers and did not largely impact data when rounding to the nearest hundreths. The overall analysis of school spending, school size and school type remained stable.



