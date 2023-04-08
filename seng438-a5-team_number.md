**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group \#: 10              |  
| ------------------------- |
| Student Names:            |     
| Saina Ghasemian-Roudsari  |     
| Ana Perrone               |     
| Rachel Dalton             |     
| Isaiah Lemieux            |

# Introduction
In this last assignment of SENG 438, we were once again given the opportunity to put into practice the remainder of the knowledge we have been acquiring throughout our lectures, in a hands-on approach. The focus of this assignment was to utilize different reliability assessment tools to analyze integration test data. We were expected to install one of the two options of reliability growth assessment tools and we chose the Covariate Software Failure and Reliability Assessment Tool (C-SFRAT). This is an open source application which applies covariate software reliability models. We used this tool for the first part of this assignment and we then used the Excel Worksheet and Macro: RDC-11, for the second part.

# Assessment Using Reliability Growth Testing 
Result of model comparison (selecting top two models)
----------------------------------------------------------
By using C-SFRAT we were able to import our excel sheet of faliure data set 2 into the testing tool, which generated our graph in the Model Results and Predictions section.
![NEWAllMVT](https://user-images.githubusercontent.com/76859857/230229747-27e6b89b-81d5-430b-801b-b22a1b58436b.png)


To be able to compare all the models we were able to go to the Model Comparison section. We filtered this table from the largest to smallest log-likelihood. Log-likelihood is a statistical concept that measures how well any statistical model fits a set of observed data. This means the filter we chose to generate our table by shows which model closley fits with out failure data.
![NEWComparison](https://user-images.githubusercontent.com/76859857/230229766-509cc067-748d-4d0b-8d5a-2fee83b054e9.png)


Result of range analysis
---------------------------------------
Using the Laplace transform, we completed an analysis of the failure data to determine the useful range of the data. As shown in the screenshot below, we created a graph of the Laplace transform, with the value of the transform on the Y-axis and the time interval on the X-axis. The graph represents the defects discovered over time, so to find the part of the graph which is considered reliable, we should look for a stable area of the graph with constant slope. By visually inspecting the graph, we determined that the range of useful data is between 21 and 46 on the X-axis.

![Laplace](https://github.com/seng438-winter-2023/seng438-a5-Racheld3/blob/main/Screenshots/Laplace.png)

Plots for failure rate and reliability of the SUT for the test data
--------------------------------------------------------------------
MVT Graph:
![NEWTop2MVT](https://user-images.githubusercontent.com/76859857/230229801-ced19820-35da-4a06-82d7-8c68fb2cef76.png)

Intensity Graph:

The x-axis indicates units of time and the y-axis indicates failure intensity.

![NEWTop2Intensity](https://user-images.githubusercontent.com/76859857/230229873-f69e0650-8b60-43f0-9875-e693b5df2cb6.png)

Reliability Graph: 
We used SRTAT to generate this graph.
![Screenshot 2023-04-05 153204](https://user-images.githubusercontent.com/76859857/230218702-5ba33132-5ce3-4497-9ce5-51217b0adfe9.png)


A discussion on decision making given a target failure rate
-----------------------------------------------------------------------
Setting a target failure rate is an important part of software reliability engineering. This is a benchmark for how reliable the software needs to be, thus development and testing should focus on achieving this goal. Failure data should be collected continuously to ensure that the failure rate remains at or below the target. If not, the developers should take steps to reduce the failure rate, such as further testing and debugging, a redesign of all or part of the project, or a re-evaluation of the failure target rate. 


A discussion on the advantages and disadvantages of reliability growth analysis
-----------------------------------------------------------------------------------
Advantages:
Some advantages of reliability growth analysis include efficient resource allocation. This means the graphs created can help us determine which tests and tasks are effective at improving reliability. The graphs allow us to easily pin point the impact of changes in the project as we can see changes at specific times. As well, reliability growth analysis graphs are very good at showing time-dependant trends. This is an advantage when predicting how data would behave in the future are we are able to see all past behavior.

Disadvantages:
Some disdvantages of reliability growth analysis include that when graphs are generated using different tools but the same data set for example Excel, SRTAT or C-SFRAT, the results of the graphs can often be different depending on what tool is used. As well, results can also differ based on equations used in determining target failure of the system. Reliability growth analysis can also be a very time consuming process as their is a lot of data to analyze. It can also be a costly process, since analysis can take time, and improving the reliability based on the results can take even longer and consume company resources.


# Assessment Using Reliability Demonstration Chart 
3 plots for MTTFmin, twice and half of it for your test data
--------------------------------------------------------------------
MTTFmin Plot:

![image](https://user-images.githubusercontent.com/101215683/230160531-23307e4b-423d-4f7f-96d4-35c82a11d061.png)

MTTFmin * 2 Plot:

![image](https://user-images.githubusercontent.com/101215683/230160760-4d336175-6e8e-4e24-9abe-b75752233a16.png)

MTTFmin * 0.5 Plot:

![image](https://user-images.githubusercontent.com/101215683/230160883-e204c17f-c6f6-48c2-9d7f-a40c58c2c32b.png)


Explain your evaluation and justification of deciding the MTTFmin
-------------------------------------------------------------------
When deciding MTTFmin, we wanted to make sure that all data points on the RDC using our failure data was safely in the acceptable region. In order to achieve this, we had to alter the value for our FIO (Failure Intensity Objective), the inverse of MTTF. After slowly increasing FIO until the entire chart was within the acceptable region, our resulting FIO was 67 failures per 10000 calls.

A discussion on the advantages and disadvantages of RDC Testing
-----------------------------------------------------------------
A major advantage of RDC testing is that the use of the chart provides a visual representation of a software's reliability, which makes analysis of the data and whether or not it is meeting necessary reliability levels. Additionally, because the data is charted, RDC can make the visualization of reliability trends much more obvious, which can directly affect the result of a software that is about to be deployed for the better. A disadvantage of RDC is that it may sometimes not be the best approach for testing software that may expect a low amount of failures, as the failure data sample size may not be large enough to provide a meaningful representation of the data in order to draw conclusions on the reliability of the software. Another disadvantage, RDC does not take into account external factors when representing system reliability, and therefore, sometimes might not create an extremely accurate representation of reliability.

# Comparison of Results Between Reliablity and RDC Testing

Using reliability testing tools, C-SFRAT and SRTAT, we were able to generate several graphs to model the reliability of the SUT. Firstly, using C-SFRAT, we generated an MVT graph, showing the mean time between failures over time. Based on this graph's linearity, we can see how the MTBF stays relatively constant over time, indicating that the system is fairly consistent in its reliability. Next, we generated an intensity graph showing the failure intensity over time. From this graph we can see that the failures occur at a consistent frequency, around every 10 units of time. For each graph, the most well-fitting models were applied, which fit the actual data accurately. Next, using SRTAT, we generated a reliability graph, showing time as a function of the failure number. From this graph, we can see that as the failture number increases, the time becomes exponentially larger, showing a slight increase in reliability over time. 
After entering failure data from failure set 2 into the correct cells in the RDC excel file, we then analyzed the resulting chart to deduce the MTTFmin, which we found through the FIO. The max FIO to ensure the failure data would be safely situated within the acceptable region of the chart was 67 faulures per 10000 calls. Inversely, the minimum number of calls before failure is 149 calls. Meaning that, with an FIO of 67 failures per 10000 calls, the test shows strong evidence that the SUT would acheive this FIO.

# Discussion on Similarity and Differences of the Two Techniques
For the similarity between the two techniques we utilized in this assignment, both the Reliability Growth Assessment Tools and the Reliability Demonstration Chart (RDC) aim to make sense of the failure rate of a system and what a failure means to that system as well as assess its reliability. The difference between the two is their different assessment criteria. The reliability growth assessment tool is able to measure the failure rate, MTTF and reliability of the SUT by analyzing test data. Whereas the RDC checks whether that target failure rate or MTTF is met, which then allows us to decide the adequacy of the testing. Therefore as its name suggest the reliability growth assessment tool evaluates the advancement of reliability growth, and the reliability demonstration chart helps to showcase that the system has met a specific target.


# How the team work/effort was divided and managed
We divided the team work by getting two team members to work on the Reliability Growth Testing, and the other two memebers to work through RDC Testing. Then to ensure work was done correctly for both sections and graphs were generated properly we had the two team members explain to eachother how the assesment of testing was done. Then both pairs of two switched and re-generated the graphs they were not reponsible for the first time to ensure plots were generated correctly.


# Difficulties encountered, challenges overcome, and lessons learned
Our team had a very challenging time at first trying to learn and set up the functionality of the C-SFRAT testing environment. We found it difficult at first to know how to complete the model ranking. We overcame this challenge by going through the "A covariate software tool to guide test activity allocation" link provided on the assignment sheet which provided a lot of direction on how to generate the graphs. Additionally, when introducing ourselves to the RDC excel file, even after reading the accompanying RDC overview and lecture slides regarding RDC, it was still extremely difficult to get comfortable using the RDC file, and understanding the general procedure for using it. 
One of the lessons learned while generating graphs using C-SFRAT was that we had to convert the times to hours, since the first time me generated all the plots of the graphs we used seconds and we saw that this did generate incorrect results.


# Comments/feedback on the lab itself
It would have been helpful to have some more detailed instructions about how to use Software Reliability and Testing Analysis Tools, as well as having a tool which is able to run on every type of computer.
