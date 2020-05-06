# Automate
Introduction

This project use case is that there is a developer working on the project. Now he wants another developer to work on this. So We used the concep of git branch to provide a different branch to the new developer and whenever any one commits the code is uploaded to github.

 After that jenkins has three tasks 

1:Has to keep check on the master brach and as soon as something changes the jenkins runs the job and download the code in testing environment.

2:  Has to keep check on the developer branch and as soon as something changes the jenkins runs the job and download the code in testing environment.

3: The third task is jenkins will check the code and merge the code into master branch and finally deploy the webpage after successful quality check.

For this we assumed that we already have the Webserver image, docker installed, and github account.

Step1: First we have to create the webpage using notepad in gitbash and the developer must be in master branch and then commit the file and it will use post-commit hook to automatically push to github.

Step2: Now we have to create a new branch for the another developer to modify and write code. The other developer will also do same steps as the master developer.

Step3: Now Goto jenkins create a JOB1: which will include github url, trigger,and command to launch production environment.

Step4: Create JOB2: which will be same as the JOB1 but only change will be in the port number.

Step5: Create JOB3: which will do the job of merging the two branches whenever the test passsed. And this job will be triggered manually or we can use remote trigger option and can use the url to trigger the job.

Finally  our setup of jenkins is done.

Now we have to go redhat operating system where both docker and httpd services are running. We have to create the directory for production system and the testing system respectively as mentioned in JOB1 and JOB2 for storing the webpage downloaded from the github.

Now use docker ps command to see all the running containers. You can find the production as well as testing containers running using docker containers. 

Now We can type the IP in the browser and browse the webpage.
