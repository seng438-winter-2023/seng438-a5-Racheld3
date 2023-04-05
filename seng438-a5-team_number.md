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
In a much similar fashion to the previous assignments in this course, we were given another opportunity to put into practice: the knowledge we have been acquiring throughout our lectures. We were expected to install and use a reliability growth assessment tool we chose The Covariate Software Failure and Reliability Assessment Tool (C-SFRAT). This is an open source application which applies covariate software reliability models.

# Assessment Using Reliability Growth Testing 
Result of model comparison (selecting top two models)
----------------------------------------------------------
By using C-SFRAT we were able to import our excel sheet into the testing tool, which generated our graph in the Model Results and Predictions section.
![AllModelsGraph](https://user-images.githubusercontent.com/76859857/229024877-6fec0c14-cc21-4032-adb8-4ecbf0b88225.png)

To be able to compare all the models we were able to go to the Model Comparison section. We filtered this table from the largest to smallest log-likelihood. Log-likelihood is a statistical concept that measures how well any statistical model fits a set of observed data. This means the filter we chose to generate our table by shows which model closley fits with out failure data.
![logLikelihood](https://user-images.githubusercontent.com/76859857/229024910-f9ae3991-70f9-4fe9-9a0c-c644df1050be.png)

Result of range analysis
---------------------------------------


Plots for failure rate and reliability of the SUT for the test data
--------------------------------------------------------------------
MVT Graph:
![Only2BestModels](https://user-images.githubusercontent.com/76859857/229030935-fb8accb6-54ca-4e93-9258-a21267038fa4.png)

Intensity Graph:
![OnlyBest2ModelsIntensityGraph](https://user-images.githubusercontent.com/76859857/229030983-1a4b6ac0-e457-4c4f-a15c-dffe6a69311a.png)




# Assessment Using Reliability Demonstration Chart 
3 plots for MTTFmin, twice and half of it for your test data
--------------------------------------------------------------------
MTTFmin
--------------------------------------------------------------------
![image](https://user-images.githubusercontent.com/101215683/230160531-23307e4b-423d-4f7f-96d4-35c82a11d061.png)

MTTFmin * 2
--------------------------------------------------------------------
![image](https://user-images.githubusercontent.com/101215683/230160760-4d336175-6e8e-4e24-9abe-b75752233a16.png)

MTTFmin * 0.5
--------------------------------------------------------------------
![image](https://user-images.githubusercontent.com/101215683/230160883-e204c17f-c6f6-48c2-9d7f-a40c58c2c32b.png)


Explain your evaluation and justification of deciding the MTTFmin
-------------------------------------------------------------------


A discussion on the advantages and disadvantages of RDC
-----------------------------------------------------------------

# Comparison of Results Between Reliablity and RDC Testing


# Discussion on Similarity and Differences of the Two Techniques




# How the team work/effort was divided and managed



# Difficulties encountered, challenges overcome, and lessons learned
Our team had a very challenging time at first trying to learn and set up the functionality of the C-SFRAT testing environment. We found it difficult at first to know how to complete the model ranking. We overcame this challenge by going through the "A covariate software tool to guide test activity allocation" link provided on the assignment sheet which provided a lot of direction on how to generate the graphs.


# Comments/feedback on the lab itself
It would have been helpful to have some more detailed instructions about how to use Software Reliability and Testing Analysis Tools, as well as having a tool which is able to run on every type of computer.
