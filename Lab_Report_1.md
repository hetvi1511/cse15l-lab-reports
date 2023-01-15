# **REMOTE ACCESS**

Firstly, let's get a brief of how and why remote access is important and how beneficial it can be. The purpose of remote connect is that it allows you 
to virtually use any computer or device after establishing a connection with it.\
Now to remotely connect YOUR system to the CSE Basement systems you'll need to keep a few things in mind.
- You will have to keep your CSE 15L, course specific account name handy.\
- Use your normal UCSD username and password to login into this site <https://sdacs.ucsd.edu/~icc/index.php>.\
- Once you've successfully logged in to your account, you will be asked to reset your password. Now this part can get a little tricky and time consuming.\
A few criterias to keep in mind before resetting your password.\
1) The password must be 12-30 characters long.
2) The password should contain uppercase alphabets, lowercase alphabets and special characters.
3) The password cannot contain consecutive letters and numbers.
4) The password mustn’t be your name.\ 
**TIP:** If you really don't want to change your password, make minor changes to the existing password and try resetting. There are chances that this process
may take a while.\ 
Sometimes resetting your password can be a time consuming process. The system will either not approve the password you reset and ask you to make a
new one again and if and once it approves the new password it will take around 15-20 minutes for the new password to be finally updated in the system 
and your account will be in use again. But it can take more than 15-20 minutes, so just be patient :).\
\
Now that we have completed the few necessary steps to complete the remote connection smoothly, we can proceed. 
There are 3 major steps involved in this process, they are as follows:\
- Installing VScode
- Remotely Connecting 
- Trying Some Commands\
We will go over these steps one by one so that there's no confusion and the process goes by as smoothly as it possibly can :)\
\
\
## **STEP 1:** *Installing VScode* \
\
If you are a CSE Major or have previously taken any CSE courses, you are most likely to already have VScode on your system. But if you don't, you have 
nothing to worry about. You can visit this site [Link](https://code.visualstudio.com/) and read the instructions and complete the download of VScode on
your system. They have listed how to download the application for all major operating systems.\
When you open VScode after the download is complete, you will see such a window open.\
\
![](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/VScode.png)\
\
The color of the window may differ. If you choose to keep light mode then the window that is opened will be white in color and if you choose to keep dark mode
then the window will appear dark.\
\
\
## **STEP 2:** *Remotely Connecting*\
\
This step now has fairly become easier because we have directly and indirectly explained what you will "Need". Let's dive right into it.\
Now to use ssh, open a new terminal on VScode and add a similar command of this same format.\
\
![](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/ssh.png)\
\
This address has to be replaced by your course specific. You have to add "@ieng6.ucsd.edu" after typing your course specific username.\
\
Since, mostly this is the first time you're connecting to the server you will see this prompt. It will ask you if you are sure you want to
continue connecting, answer yes and proceed to the next step. Next step is just entering the password that you reset before starting these major steps. 
When typing in the password be very careful, because you will not be able to view what you're typing in the terminal. If you feel like you've 
made a mistake then press backspace for a while till you're confident that everything you've typed has been deleted.\
\
![](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/password.png)\
\
After typing the password and if the connection is successful, this is what will appear on the screen.\
\
![](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/connection_success.png)\
\
This means you've successfully connected your device to a remote server. GOOD JOB !!\
\
\
## **STEP 3:** *Trying Some Commands*\
\
Now we can test some basic commands and get an idea of what to expect as the output. In CS not getting any error or any message is most of the time a
good sign. Some of the commands we run will give no output and that is okay, it doesn't mean anything is wrong, that's the desired response we should
be expecting. Here are a few of the commands you can try:\
- cd ~
A common mistake made with this command is not adding a space between "cd" and "~".\
\
This is what you'll see after the command is executed successfully\
![](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/cd%20~.png)\
\
- ls -lat \
This is what you'll see after the command is executed successfully \
![](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/ls%20-lat.png)\
\
- cat /home/linux/ieng6/cs15lwi23/public/hello.txt \
This is what you'll see after the command is executed successfully \
![](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/cat.png)\
\
\
This brings us to the end of setting up the remote connection. If there are any questions or you see different prompts on your screen, always feel free 
to ask the tutors. They are always ready to help and give very helpful tips.\
\
Good Job ! You're done with your first lab.\
