# Covid Vaccine Tracker
Overview: 
In this project, I aim to make the process of booking a vaccination slot on the Cowin portal easier by notifying the user whenever a slot is available in his neighbourhood. Due to the enormous gap between demand and supply of vaccines in India, one often finds it very difficult to book an appointment for vaccination. For some people (including me), it took several hours to book the appointment. So to save valuable time, I thought of making a simple program that will send an email to the user when vaccination is available in his neighbourhood. 
For this project, I used the following python libraries:
tkinter
smtplib
BeautifulSoup
requests
time

I used tkinter to create a minimalistic user interface so that users do not need to give the input every time by opening an IDE or command prompt. For sending email to users, I used some functions like ehlo(), sendmail(), starttls() and login() from the smtplib library. These functions are used to send the email containing information about the vaccination centre having the maximum number of doses in the user given Pincode. To collect the data from the API Setu, I used BeautifulSoup and stored that data in a string; the data contained many unnecessary parts that had to be removed. This process of removing unwanted data is done by a function called str_to_list(). Then to check for the centre containing the maximum number of doses for the user-provided age group, I wrote a function called is_available(). 
Finally, all this process is nested inside an infinite while loop as the website might get updated every second. To avoid memory issues, I used the function sleep from the time library, which will pause the loop for some time after completing one successful iteration. 
The features that I am thinking to implement in future are as follows:
Hosting it on a server and creating a website or app so that someone who does not have python installed on their machine can still use it. 
Adding more inputs for Pincode. 

How to install:
Download the source code from my Github repository.
If you do not have python installed on your PC, download it from https://www.python.org/.
Download the required libraries. 

How to use:
1.	Simply run the code. A window will appear as follows: 



2.	Fill in the information and click on the submit button.
(use the DD-MM-YYYY format for date). Sample input is given below.











3.	Now, if the vaccine is available, the user will receive an email as follows:



4.	If no vaccines are available for the given date and Pincode, you should get a dialogue box as shown below:



