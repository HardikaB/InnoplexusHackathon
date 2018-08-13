# InnoplexusHackathon
Classification of Web page

Problem Statement
Classification of Web page content is vital to many tasks in Web information retrieval such as maintaining Web directories and focused crawling. The uncontrolled nature of Web content presents additional challenges to Web page classification as compared to traditional text classification, however the interconnected nature of hypertext also provides features that can assist the process.

Here the task is to classify the web pages to the respective classes it belongs to, in a single label classification setup (Each webpage can belong to only 1 class).

Basically given the complete html and url, predict the tag a web page belongs to out of 9 predefined tags as given below:

  1) People profile
  2) Conferences/Congress
  3) Forums
  4) News article
  5) Clinical trials
  6) Publication
  7) Thesis
  8) Guidelines
  9) Others
  
Data Dictionary
train.zip contains 2 csvs
1.	train.csv: Train set 
Variable	Definition
Webpage_id	Unique ID for the Web page
Domain	Domain
Url	Complete Url
Tag	(Target) Tag (Class) of the Web page
2.	 
3.	html_data.csv: Contains web page data in HTML for both train and test web pages 
Variable	Definition
Webpage_id	Unique ID for the Web page
Html	Web page data in HTML
4.	 
 
test.csv: Test Set 
Variable	Definition
Webpage_id	Unique ID for the Web page
Domain	Domain
Url	Complete Url
 
 
sample_submission.csv: Submission format 
Variable	Definition
Webpage_id	Unique ID for the Web page
Tag	(Target) Tag (Class) of the Web page
Train-Test Split
The tr¬¬ain and test data split is done based on Domain-Tag combination. For example, suppose we want to split the following sample of 16 URLs into train and test set.
 
 
  
•	First the overall dataset is split into subsets by Tag as shown below:
 
•	Now for each subset(Tag) we store all unique domains and randomly shuffle them, so in this case lets say we have:
 
 
  
•	Next, every third domain (3rd, 6th, 9th and so on) in the all domain sequence is assigned to the test and the rest (1st, 2nd, 4th, 5th, 7th and so on) are assigned to train as shown in the following table:
 
  
•	Final train and test set would be:
 
 
  
Evaluation Metric
The evaluation metric for this competition is weighted F1 score.
  
Public and Private Split
Test data is further randomly divided into Public (40%) and Private (60%) data. 
•	Your initial responses will be checked and scored on the Public data.
•	The final rankings would be based on your private score which will be published once the competition is over.
