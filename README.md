# CS3SY26_ProjectProposal by Magallona, Mamutuk, Paraon, of 9 - Beryllium



### Project Title or Name of the Application	: River Quality Scorer
### Section			   	      : 9 - Beryllium
### Group Members			    : Magallona, Mamutuk, Paraon
### Date (Proposal Date)  : Nov 13 2026
### Project Description:

- The River Quality Scorer is designed to score the water quality of rivers according to measured and observed characteristics of water into a 1-10 scale, along with a brief report. This application takes in user data and simplifies it into a score, helping users compare their chosen river to a healthy river. Users will input measurements that serve as factors such as pH, turbidity, temperature, dissolved oxygen, and the program will calculate a score, and infer what has happened, or what will happen to the environment based on how the score was calculated. For example, a low dissolved oxygen measurement can be caused by pollution and can cause aquatic death.

The project is needed as the River Quality Scorer turns complicated data into a simplified report which can be interpreted by anyone. The report can help communities understand their rivers, the problems and changes that might worsen river health, and furthermore, communities will create better decisions to protect the environment.
  
- The user inputs water sample data into the Water_sample class to store it, and passes it off to a scorer which compares it with user supplied healthy ranges and minuses if one attribute is off. Water sample data is also passed off to another class, class ConcernTracker, which returns concerns about certain attributes, such as the cause and effect of an unhealthy water quality attribute. The reportCreator class stores the output of Scorer and ConcernTracker and combines it into a simple readable text for the end user.

Class WaterSample
Attributes:
pH		- stores pH level,
Turbidity	- stores Turbidity level,
Temperature   - stores Temperature,
Dissolved_oxygen - stores dissolved oxygen levels,
Methods:
data_validation()- check if its within the measurement range,
data_get() - return all stored information for processing as a dictionary
	
Class Scorer
Attributes: 
Data - takes data from class WaterSample,
Healthy_ranges - User inputs their own healthy ranges as a dictionary,
Methods:
calculate_score() - checks a data reading against the healthy range and minuses to the score and returns the total,
evaluate_parameter() - checks a data reading against the healthy range and returns the attribute that flagged it

Class ConcernTracker
Attributes:
Identified_concerns - takes the attributes that got flagged from evaluate_parameter() from class Scorer,
Methods: 
Show_concerns()-determines which measurements indicate river health problems	,
Show_effects()- describe impact (e.g. environment),
Show_causes()-show reasons for poor measurements,

Class ReportCreator
Attributes: 
River_score - takes the river score total from calculate_score() from class Scorer,
Concerns - takes the output of Show_concerns from ConcernTracker,
Effect - takes the output of Show_effect from ConcernTracker,
Causes  - takes the output of Show_causesfrom ConcernTracker,
 
Methods:
display_report() - this generates and compiles the data and will print the report when called

- The River Quality Scorer is intended for anyone like students, science teachers, environmental organizations, community groups, and members of the public who are interested in understanding river health. Many users may be able to collect water quality measurements such as pH, turbidity, temperature, and dissolved oxygen, but may not have the scientific knowledge and method required to interpret the data, aiming to help these users by simplifying water quality data into simple and understandable reports with river quality score. This educates the user and allows them to identify potential environment issues and make sensible decisions about river conservation and water management.
 

- The description is then followed by the class diagram, depicting clearly what was described.

### Goals:

Describe the long term outcomes of your project followed by a couple of objectives to meet the goals stated in this paragraph

- Objective 1:
- Objective 2:
- Objective n:

[Click here for Rubrics and Sample projects](https://docs.google.com/document/d/1xKd1CqK6DcNWS2_oJPBNtY5n3I3Hqiw8FY3W295Iqfk/edit?usp=sharing)
