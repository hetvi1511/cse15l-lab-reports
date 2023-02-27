# Lab Report 4


This week we had a very different Lab session compared to the previous ones. We had a competition environment setup. They gave us a task in the 
starting of the lab session and gave us 1 hour to prepare for those tasks. Then we had to compete with each other, whoever did it the fastest proceeded 
to the next round and finally a winner would be announced.\
The steps we were asked to do were as follows:
> 1. Setup Delete any existing forks of the repository you have on your account
> 2. Setup Fork the repository
> 3. The real deal Start the timer!
> 4. Log into ieng6
> 5. Clone your fork of the repository from your Github account
> 6. Run the tests, demonstrating that they fail
> 7. Edit the code file to fix the failing test
> 8. Run the tests, demonstrating that they now succeed
> 9. Commit and push the resulting change to your Github account (you can pick any commit message!)
** NOTE ** : I had already setup generating a SSH Key of ieng6 and GitHub, which allowed me to login without using a password. This helped me do the tasks 
quicker.\
## Step 1- Step 3
While making the report I was doing this challenge again. So I had to delete the lab 7 repository and re-fork it.\
To delete the repository, open the lab 7 repository if you have forked it earlier. Go to settings, and scroll to the bottom of the page. You will see an
option of delete this repository. Click on it and this will be the pop-up.\
![delete](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/delete.png)\
Write the name of the repository and click on "I understand the consequences, delete this repository"\
To fork this repository again, go to [Lab 7](https://github.com/ucsd-cse15l-w23/lab7) and click "Fork" near the top right. Then this will pop-up.\
![create](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/refork.png)\
Click "Create fork" and you are all set.\
After this is done, you are now set to start the challenge and time yourself :)
## Step 4: Logging in to your course specific account
We always login in to our course specific account before doing any tasks. We do the sme for this challenge. But this time we don't need a password because
we have created a SSH Key for our ieng6 and GitHub accounts.
```
ssh cs15lwi23apo@ieng6.ucsd.edu
```


After typing this command press <enter>/<return> and the output you will see will be as follows:
![login](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/login.png)
## Step 5: Cloning the forked repository
For cloning the repository, use the following command-line command:\
```
git clone https://github.com/ucsd-cse15l-w23/lab7
```
This is the message that will be displayed after successfully cloning the repository.
![clone](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/clone.png)
## Step 6: Run the tests, and show that they fail
To run the tests, first make sure that your current directory is lab7. I changed my directory to lab7 and ran the tests.
```
cd lab7/
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```
I copy pasted these commands. So I used <Cntrl-C> to copy and <Cntrl-V> to paste these commands.\
The message that was displayed on the terminal was as follows:\
![runtest](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/runningtests.png)
## Step 7: Editting the code
We need to fix the error for the tester to run correctly. To do that, we type the following command:
```
nano ListExamples.java
```
This opens the code in the terminal and allows us to edit the program. Refer the image below and make the required changes to your code for it to test 
successfully.
![nano](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/nano.png)\
After editting the code, press <Cntrl-O>, <enter>, <Cntrl-X>. This combination of commands saves the file and exits.\
(The first command is pressing Control and then the alphabet o).\
## Step 8: Re-running the tests
Now to check if our modified code runs properly, we need to run the tests again. For that, we type the following commands again.
```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```
You can use <up> and <enter> to make the process faster.\
This is what is displayed after running the tests again.\
![rerun](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/rerun.png)\
## Step 9: Commit and Push the changes to your account
Type the following commands, in the same order. Refer to the image below to understand what to exoect at the terminal after every command.\
```
git add ListExamples.java ListExamplesTests.class
```
```
git commit -m "Fixed"
```
```
git push git@github.com:hetvi1511/lab7.git
```
The "Fixed" in the second command can be anything you want, it should be something to indicate that you have changed the code, and now the tests work.\
For the last step, the git link will be copied from your github account, in the lab7 repository.\
This is what is displayed at the terminal after every step.\
![commit](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/commit.png)\
Don't forget to time yourself :))
