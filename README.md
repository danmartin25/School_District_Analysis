# School_District_Analysis

## Project Overview
The school board suspects academic dishonesty. They bring this to the attention of Maria and her supervisor. The specific charges are that the reading and math grades for Thomas High School have been altered. Maria has asked us to analyze the data as is, and with the 9th grade scores for Thomas High School removed. Our goal is to look at any differences between the two analyses and give our opinion about the possible altering of the 9th grade scores for Thomas High School.

## Resources
- Data Source: schools_complete.csv and students_complete.csv
- Software: Python 3.10.0, Jupyter Notebook 6.3.0

## Results

### How is the district summary affected?
The district summary itself is not heavily affected, likely due to the relatively small number of 9th grade students at Thomas High School when compared to the students of all schools in all grades in the district.

Here is the summary with the 9th graders' scores intact:
![district_summary_without_removal](https://user-images.githubusercontent.com/91795475/140632992-16b32fe1-258d-41a8-9b39-ba29239fb1d8.PNG)

Here is the summary with the scores removed:
![district_summary_with_removal](https://user-images.githubusercontent.com/91795475/140633005-02f5ca24-f621-494e-af8c-a2d9ed0b3f18.PNG)

### How is the school summary affected?
The school summary for Thomas High School is affected much more.





Here is the summary with the 9th graders' scores intact:

![school_summary_without_removal](https://user-images.githubusercontent.com/91795475/140633444-d27b4e98-b6c1-4cd8-84da-0d012b0966b9.PNG)





Here is the summary with the scores removed:

![school_summary_with_removal](https://user-images.githubusercontent.com/91795475/140633446-6e2880bc-a967-42a5-8f71-7ce5a882c6a2.PNG)




We can clearly see something is wrong. The percent of 9th graders passing is way too low. Just by removing them from the data, which is only about 1/4th of the total students in the school, the passing percentages jump up over 20% for math, reading, and overall. A statistical analysis would have to be done to determine this for certain, but we would be willing to bet that the difference is statistically significant, especially when we consider that the average math and reading scores are the same (up to 8 significant digits!) whether we remove the data or not. The data is showing us that some scores were increased a lot, and a lot of scores were decreased to less extreme values. If we graphed the individual 9th graders scores, we would expect there to be a heavy skew upwards to compensate for all of the students failing below the 70% line (because the average score stays the same).


### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
With the scores removed, Thomas High School posts very good passing rates, good enough for second overall. As shown previously, the average scores were not affected, but those were good as well. Below are the average scores where Thomas High School is at the beginning of the pack.

Math Scores by Grade:


![math_scores_by_grade](https://user-images.githubusercontent.com/91795475/140634039-09239790-9e3f-4379-936f-25f36f3aa18e.PNG)


Reading Scores by Grade:


![reading_scores_by_grade](https://user-images.githubusercontent.com/91795475/140634035-52fba95c-5f97-4988-8cff-9e806a7381af.PNG)



What we can infer from these charts is that Thomas High School has a similar looking distribution to the other schools and we would not expect this drastic of a change to happen naturally. It is important to note here that Thomas High School is a charter school. There is a significant distinction between the passing rates of charter schools and district schools. With the 9th graders removed, Thomas High School is 2nd in overall passing percentage. With their scores, Thomas High School dropped to dead last in overall passing percentage out of all of the charter schools. Here is the list of charter schools (with overall passing percentage in the column all the way to the right). This is shown with the scores removed, but we know from the chart before that their overall passing percentage drops to 65% with the 9th graders' scores.


![overall passing percentage relative](https://user-images.githubusercontent.com/91795475/140634228-2fb6dee8-69c7-4de5-bd40-8441518a49a1.PNG)



### How does replacing the ninth-grade scores affect the following:

#### Math and reading scores by grade
- The average scores stay the same
- The percent of passing students drops over 20% in both categories for 9th graders at Thomas High School

#### Scores by school spending
- The average scores stay the same, so spending per average scores stays the same
- Due to a larger sample size, the passing rates by spending does not change as much as we think it would. As skewed as the results are, they are still only from one grade at one school out of 15 schools. 

Here are the numbers for the different spending ranges with removal of the 9th graders' scores:

![per_capita](https://user-images.githubusercontent.com/91795475/140634356-f235cd22-0808-422a-9f1b-f7dc16d1a70d.PNG)


#### Scores by school size
- There is no change in the average scores.
- Again, the change in the percentage of passing scores is determined by the sample size. Since many of the charter schools are smaller schools, including Thomas High School, we are looking at a small sample in a small population. The percentages should go down, but not too heavily.

Here are the numbers for the different size ranges with removal:

![school_size](https://user-images.githubusercontent.com/91795475/140634591-45ee556e-e9dd-4d47-afad-5f020269e3f0.PNG)



#### Scores by school type
- There is no change in the average scores.
- District schools will not be affected since Thomas High School is a charter school. The percentage of passing grades will take a hit and it should like almost identical to the difference when we looked at school size. Again, the difference will not be that big in the big picture, but if something like federal aid was proportional to these numbers the difference could be more important.

Here are the numbers for the different types of schools with removal:

![type_of_school](https://user-images.githubusercontent.com/91795475/140634673-10973d84-4b91-40f0-87e0-f51ceeb4907d.PNG)

## Summary
Four changes affected by the replacing of scores for 9th graders at Thomas High School:

- Overall passing percentage (as well as math and reading passing percentages) jumps up significantly for Thomas High School
- Overall passing percentage jumps up slightly for charter schools, and small schools.
- Thomas High School jumps up to #2 on the list of schools with the highest overall passing percentage. They were previously last of the charter schools.
- There are less total students at Thomas High School, so the numbers for spending per student will increase due to the budget staying the same.
