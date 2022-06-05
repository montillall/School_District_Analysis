# School_District_Analysis

## Overview of the School Distict Analysis

The school district analysis consists of preparing standardized test data from a variety of sources and formats for analysis, reporting and presentation to provide insights about performance trends and patterns. The insights are used to inform discussions at the school and district level and assist the school board reagarding school budget and priority. 

The objectives of the initial analysis was to analyze data on student funding and students standardized test scores, aggregate the data and showcase trends and school performance.

However, the school board has notified that the students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards. 

Based on this notice, the objective of the following analysis is to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Once the math and reading scores have been replaced. It is expected to repeat the school district analysis that has been initially done and describe how these changes affected the overall analysis. 

---
## School District Analysis Results

In order to complete the objectives of the election audit, the following script was built:

* Added dependencies csv and os to read/write .csv and txt files and get their paths 

		import csv
		import os
	
* Added two variables, one to load a file from a path and another to save the file to a path 

		file_to_load = os.path.join("Resources", "election_results.csv")
		file_to_save = os.path.join("analysis", "election_analysis.txt")

* For the total votes casted in the congressional election:
	* The variable total_votes counter was initialized to 0
	
			total_votes = 0
		
	* The data set in the csv file is open and read with the following code
	
			with open(file_to_load) as election_data:
    				reader = csv.reader(election_data)
			
	* For loop was created in order to go through each row and add the total vote count
	
			for row in reader:
 				total_votes = total_votes + 1
	
The results showed that the total votes casted were 369,711

![](Images/Total_Votes.png)

* The number of votes and percentage of total votes for each county was estimated as follows:

	* A county list and a county dictionary were created
  
			county_options = []
			county_votes = {}
    
	* An if statement created to check if a county name doesn’t match an existing county in the county list then the county name is added to the list of counties. The county’s vote starts tracking and adding votes to that county’s vote count
  
       		if county_name not in county_options:
		
            		county_options.append(county_name)	
      				county_votes[county_name] = 0
 				county_votes[county_name] += 1
      
	* For the percentage a for loop was created to get the county from the county dictionary. The county vote count was retrieve and the percentage of votes for the county was calculated 
  
		  for county_name in county_votes:
        	votescounty = county_votes.get(county_name)
        	votescounty_percentage = float(votescounty) / float(total_votes) * 100

The breakdown of the number of votes and the percentage of total votes for each county is shown in image below:

![](Images/County_Votes.png)

* The county with the largest amount of votes was determine using an if statement:

    	  if (votescounty > winning_county_count):
            	winning_county_count = votescounty
            	winning_county = county_name

The largest county turnout was Denver, see image below:

![](Images/Largest_County_Turnout.png)

* The number of votes and percentage of total votes for each candidate received was determined using the same logic as for each county, the code is show bellow:

		candidate_options = []
		candidate_votes = {}

    
    
        if candidate_name not in candidate_options:
          candidate_options.append(candidate_name)
          candidate_votes[candidate_name] = 0
          candidate_votes[candidate_name] += 1

    
        for candidate_name in candidate_votes:
              votes = candidate_votes.get(candidate_name)
              votes_percentage = float(votes) / float(total_votes) * 100

The breakdown of the number of votes and the percentage of total votes for each candidate is shown in image below:

![](Images/Candidates_Votes.png)

* The candidate that won the election with its respective vote count and percentage is show below and it was determined with an if statement
 
![](Images/Winner.png)

The results of the audit was written and saved in the election_analysis.txt file in the analysis folder

![](Images/Results_Audit_TXT.png)


---
## School District Analysis Summary

* One way to use this script for any other election would be to modify the script to be able to use a generic csv name as oppose to a given specific name.


---
