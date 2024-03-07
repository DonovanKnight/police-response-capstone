# Police Incident Coverage 
*Capstone Project for Cohort DA10 at Nashville Software School* 

### **Contents**  
- [Motivation](#Motivation)
- [Data Sources and Tools](#Data-Sources-and-Tools)
- [Data Analysis](#Data-Analysis)
- [Challenges](#Challenges)
- [Conclusions](#Conclusions)


### **Motivation**   
I initially started this project because my father is a police officer. After the riots that happened in 2020, I felt like the public view on police was slandered. It was speculated that police in our city responded to the calls of certain groups of people differently, based on certain characteristics. This project allowed me to dig into police coverage times in different demographic areas of the city, to see if there were truly differences among them. After viewing what my data told me on that topic, I decided to go further, and look at police incident coverage on a wider scale to see if any other patterns arose for the entire city.

*Back to [Contents](#Contents)*

### **Data Sources and Tools**   
**Data Sources** 

Census Data: (https://censusreporter.org/)

From here I pulled information on the income and racial spread of the residents in Nashville in 2023.

Police Data: (https://www.nashville.gov/departments/police) & (https://data.nashville.gov/Police/Metro-Nashville-Police-Department-Incidents/2u6v-ujjs/about_data)

From here I pulled the data about the police and there coverage times for all of 2023

**Tools**

Excel for cleaning the data

Python/Jupyter Notebooks for cleaning and analysis of the data 

Power BI for data visualization

*Back to [Contents](#Contents)*

### **Data Analysis**

First, I wanted to take a look at how police coverage times compared to the different incomes and races of the people in Nashville. I obtained Excel sheets of the income and races of the people. After reading them into Python/Jupyter Notebook, I grouped them by Upper Class, Middle Class, Lower Class, White, Black, and Other, respectively. I also obtained data from an Excel spreadsheet about the police, that I then read into Python/Jupyter Notebook. This information was filtered down to calls for service that were in the year 2023, calls that were dispatched, closed cases, and calls that did not involve a suspect on the run (due to the potential of an extremely long police coverage time as a result). Then I combined all this data into dataframes that were converted to `.csv` files. These files were loaded into Power BI for visualizations.

*Back to [Contents](#Contents)*

### **Challenges**
The main challenges I had were getting the police coverage times (per minute and per hour) and figuring out how to get rid of outliers in the police datasets efficiently. The coverage times were the datetime data type, and needed to be converted so I could perform numerical operations on them. But this proved to be fairly easy after help from stackoverflow.com and my peers. Tackling the second challenge however took some time. At first, I used the mean to calculate average coverage time for the police. But there were outliers making the data seem unrealistic, with most average times taking anywhere from 5-6 hours to completely handle each call for service. I also could not reasonably go through the data set and remove all the outliers because there were about 53,000 calls in Nashville within the parameters I had set. So I took the median of all my coverage and call for service numbers because it grabbed the most equidistant number between the two extremities of whatever metric I was cleaning, even with the outliers.

*Back to [Contents](#Contents)*

### **Conclusions**
The findings seem to indicate that police in Nashville DO NOT discriminate against those of different races or incomes. 

ALL times for complete coverage of ALL crimes (apart from suspects on the run) averaged between about 1 and 3 hours. 

It also appears that calls on situations that are nonviolent are handled slightly faster than those that are not.

Nashville police appear to be slightly quicker in lower income areas and areas with more minorities even though there is not a large spread of time taken between those areas and their counterparts.





