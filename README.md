# Survey-Data-Analysis

This data is from an online survey that was answered by some people within the data space. It contained questions such as Salaries, Job Title, Favourite programming language etc

To begin with, I imported the data which was in an excel file into Power Query Editor for transformation since it wasn’t a clean dataset. I began the transformation by deleting empty columns and rows. I also checked for duplicates and ensured all columns were in the appropriate data type. In the survey, for example within the Job Title column, there were some title options for participants to select whiles there was another option named “Other(Specify)” where the participant had to select this and specify their title if they couldn’t find it within the title provided. This resulted in a lot of messy data as several other job titles were specified. To take care of this, I decided to group all specified titles into one category and named it “Others” for the purpose of my analysis. I achieved this by using the Split Column by Delimiter function since the specifications where closed in parentheses ie Other (Job title), in which case you can simply use the opening parentheses as your delimiter to split the remaining characters into another column then deleting it. Same thing was done for the columns Favorite Programming Language and Country. However, there could be other ways to handle this depending on what analysis one is trying to achieve.

For the Annual Salary columns, most of the values inputted by participants where in ranges hence I had to find the average salary. I did this again by splitting the columns with a delimiter and finding the average in a new column using Power Query’s powerful M Language.

After I was convinced I had a clean data, I loaded it into Power Bi for visualization and analysis.

Below is a chart showing some interesting findings.

<img width="684" alt="Capture d'écran 2024-02-20 193345" src="https://github.com/PenguinAretha/Survey-Data-Analysis/assets/97256031/5bec1ef7-4970-4ff8-a3c9-218821630ac8">

In all 630 people took part in the survey as shown with an average age of 28.87. From the Treemap as well, we can see majority of participants are from the United States and the Category grouped as Others. Data Scientists tend to earn higher than their counterparts in the data field with Data Analyst earning the least. Python has always been touted as the preferred programming language in the data domain and evidence can be seen from this survey as it clearly dominates the other programming languages. One of the positives in this survey is the fact that female participants on average earned more than their male participants.

Recommendation

Depending on your use case and what analysis you’re looking to undertake, it wouldn’t always be advisable to replace specified fields with a general category as this can lead to discrepancies within your analysis. As in a case of average salary, it can be seen that Data Analyst have the least average salaries. However, this might not be true to some extend considering the fact that several other professions were classified into “Other” category.
