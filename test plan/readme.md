#Test plan identifier  
#Project Test plan Online Book Store 
2. Introduction 
 
The goal of this document is to develop a test plan for the Online Book Store design system. This document defines all the procedures and activities required to prepare for testing of the functionalities of the system which are specified in Vision document. The objectives of the test plan are to define the activities to perform testing, define the test deliverables documents and to identify the various risks and contingencies involved in testing. 
 
3. Features to be tested  
 
The following list describes the features to be tested:  
 
USER: 
•	Registration 
•	Login 
•	Add To Cart 
•	Edit Cart 
 
ADMIN: 
•	Create and Delete book from Category 
•	Create and Delete a Category 
•	Manage Orders 
•	Manage Members 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
4.   Test Cases 
 
4.1 USER 
 
 
Registration 
 
  ID  	TEST CASE 		USER INPUT 	PASS CRITERIA 
U_REG_1 	User Registration 	User 	selects 	already  existing user name 	Display  message  to choose different user name 
U_REG_2 	User Registration 	User enters different password in password 
confirm field 	Display message  that 
Password and Confirm Password fields don't match 
U_REG_3 	User Registration 	User forgets to enter a particular required fields 	Display message The value in field is 
required 
U_REG_4 	User Registration 	User enters all the details successfully 	User account created 
 
Login 
 
  ID  	TEST CASE 		USER INPUT 	PASS CRITERIA 
U_LOG_1 	User Login 	User 	enters 	a username 	wrong 	Display message Login or 	Password 	is incorrect. 
U_LOG_2 	User Login 	User 	enters 	a password 	wrong 	Display message Login or 	Password 	is incorrect. 
U_LOG_3 	User Login 	User enters correct  username and password 	User 	logs 	in 
successfully 
 
Add to Cart 
 
  ID  	TEST CASE 	USER INPUT 	PASS CRITERIA 
U_AC_1 	Add to Cart 	User selects a book and clicks add to cart button 	Book is added to the shopping cart 
U_AC_2 	Add to Cart 	Guest selects a book and clicks add to cart button 	User should create an account. 
 
 
 
 
 
 
 
 
 
 
Edit Cart 
 
  ID  	TEST CASE 		USER INPUT 	PASS CRITERIA 
U_EC_1 	Edit Cart 	User changes the Quantity 	Quantity and total cost 
of 	Cart 	should 	be 
updated 
U_EC_2 	Edit Cart 	User deletes a book from shopping Cart 	Books and total cost of 
Cart should be updated 
U_EC_3 	Edit Cart 	User selects a new book to shopping Cart 	Books and total cost of 
Cart should be updated 
 
 
4.2 ADMIN 
 
Create and Delete a Book from Category 
 
  ID  	TEST CASE 		ADMIN INPUT 	PASS CRITERIA 
AD_CDB_1 	Create and Delete a 
Book from Category 	Admin adds a new book to category 	Book 	should 	be updated in Categories list 
AD_CDB_2 	Create and Delete a 
Book from Category 	Admin deletes  a book from category 	Book should be deleted in Categories list 
 
Create and Delete a Category 
 
  ID  	TEST CASE 		ADMIN INPUT 	PASS CRITERIA 
AD_CDC_1 	Create and Delete a 
Category 
 	Admin 	adds 	a 	new 
category 	Category 	should 	be updated to system 
AD_CDC_1 	Create and Delete a 
Category 
 	Admin deletes a  category 	Category should be deleted from system 
 
 
 
 
 
 
 
 
Manage Orders 
 
  ID  	TEST CASE 	ADMIN INPUT 	PASS CRITERIA 
AD_MO_1 	Manage Orders 
 
 	Admin accepts an order 	Order is processed 
AD_MO_2 	Manage Orders 
 
 	Admin deletes  an order 	Order is not processed 
 
 
 
 
Manage Members 
 
  ID  	TEST CASE 	ADMIN INPUT 	PASS CRITERIA 
AD_MM_1 	Manage Members 
 
 	Admin accepts Members 	Member is accepted 
AD_MM_2 	Manage Members 
 	Admin deletes  Members 	Member 	is 	not 
accepted 
 
 
 
 
 
5. Approach  
 
This section describes the overall approach of the testing which ensures that the each feature and the combination of the features are adequately tested. The major tasks that are used are 
 
5.1   Unit testing 
 
Unit testing is a method of testing that verifies the individual units of source code  are working properly. The goal of unit testing is to isolate each part of the program and show that the individual parts are correct. The NUnit a testing tool for C#, will be used for unit testing. 
 
 
 
5.2 Load testing 
 
Load testing is the process of creating demand on a system or device and measuring its response. It generally refers to the practice of modeling the expected usage of a software program by simulating multiple users accessing the program concurrently. As such, this testing is most relevant for multi-user systems; often one built using a client/server model, such as web servers  
5.3 System Testing 
 
Once the entire system has been built then it has to be tested against the Software Requirement Specification and System Specification to check if it delivers the features required. System testing can involve a number of specialist types of test to see if all the functional and non-functional requirements have been met.  
 
 
5.4 Performance Testing 
 
The system should meet the performance requirements as mentioned in the Vision document. The performance will be evaluated based on the response time of the GUI and the database commands. Using JMETER tool performance testing will be done. 
 
5.5 Manual Testing   
 
Manual Testing will be done to ensure the correctness of various parts of the code using test cases generated by the tester. 
 	 
6. Pass/fail criteria 
 
The system should satisfy all the functional requirements, in the Vision document. 
Each feature to be tested will be evaluated against its requirement as stated in the Vision Document. The pass or fail of a test depends on whether the system meets with all the particular post conditions. 
Test cases executed on the Online Book Store will pass if they meet the specific requirements as mentioned in the Vision Document. 
7. Suspension criteria and resumption requirements  
 
7.1 Suspension criteria  
 
If the system contains one or more critical defects like the defects in the GUI editor which provides the editing features for one line diagrams and database locking, unlocking and sharing features which provides the environment for multiple users to work in parallel, the entire system should be suspended. 
 The testing may also be suspended if the hardware and software components required are not available on time. 
The failed test cases should be recorded along with the description for failure.  
 
7.2 Resumption requirements  
 
When a new version of the system is transmitted to the test group after a suspension of testing has occurred, all previous tests will be rerun to ensure program changes have not inadvertently affected other portions of the program. 
8. Test deliverables  
 
The following documents are the available test deliverables:- 
•	Test plan 
•	Test case specifications 
•	Test input and output data 
•	Test procedure specifications 
•	Test logs 
 
References 
1.	http://en.wikipedia.org/wiki/Load_testing 
2.	http://en.wikipedia.org/wiki/Unit_test 
 
 
 
 
