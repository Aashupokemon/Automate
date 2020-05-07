# Automate
DevOps Task by VIMAL DAGA SIR
Pre-requisite :
OS: Base OS is Windows 10. Server OS is RedHat Enterprise Linux 8 (RHEL8) in Virtual Box.
In RHEL8 some of the softwares needed are Docker (also need the httpd image downloaded in it), Jenkins (also github plugin should be installed in it), ngrok program.
In Windows we need git bash software.
At the starting stop the firewalld in RHEL8 and start the docker and jenkins services.
Introduction:
This project use case is that there is a developer working on the project. Now he wants another developer to work on this. So We used the concept of git branch to provide a different branch to the new developer and whenever any one commits the code is uploaded to github.

 After that jenkins has three tasks 

1:Has to keep check on the master brach and as soon as something changes the jenkins runs the job and download the code in testing environment.

2: Has to keep check on the developer branch and as soon as something changes the jenkins runs the job and download the code in testing environment.

3: The third task is jenkins will check the code and merge the code into master branch and finally deploy the webpage after successful quality check.
FOLLOW THE PROCEDURE TO IMPLEMENT THE SYSTEM 
Step 1: Create github repository and from gitbash add the file to github using master branch.
Step 2: Create a branch for the developer and change the code and then again upload to github using git commit command.
Step 3: Create a jenkins production job which will copy the code into redhat server from github.
Step 4: Create a jenkins production deployment job using docker container to launch the production system.
Step 5: Create a jenkins testing job same as job1 but change the branch with developer branch.
Step 6: Create a jenkins testing deployment job using docker conatiner to launch test system.
Step 7: Create a jenkins final job for merging the two branches when quality check is successful.
This is the complete process for developing the system.
 TO TEST THE SYSTEM 
 Step 1: using the ip of the redhat and port number search for the webpage on your browser.
 Step2 : Now change something in the developer branch code and reload the browser to see chnages.
 Step 3: Now again to test for merging change something in the master branch and commit. Reload thw browser again and you will see that site is working fine.
 
 Thank you vimal sir for giving us such an amazing task.
 
