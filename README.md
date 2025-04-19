Task 8: Java Maven Build Job in Jenkins
Objective
This project demonstrates setting up a Jenkins CI/CD pipeline to build a Java HelloWorld application using Maven, hosted on an AWS EC2 Ubuntu instance with Jenkins running in a Docker container.
Tools Used

AWS EC2 (Ubuntu 22.04, t2.micro)
Docker (Jenkins container: jenkins/jenkins:lts)
Java JDK 11
Maven 3.8.6
Git

Setup and Execution Steps

Launched EC2 Instance:
Configured a t2.micro Ubuntu instance with ports 22 (SSH) and 8080 (Jenkins) open.


Installed Tools:
Installed Docker, Java JDK 11, Maven, and Git on the EC2 instance.


Ran Jenkins in Docker:
Started Jenkins container with persistent storage.
Accessed Jenkins at http://<ec2-ip>:8080.


Created Java App:
Developed a HelloWorld Java app and pom.xml in ~/hello-java-maven.
Tested locally with mvn clean package.


Configured Jenkins Job:
Set up a Freestyle job named HelloJavaMavenBuild.
Configured Maven 3.8.6 and set goals to clean package.
Copied project files to Jenkins workspace in the Docker container.


Ran Build:
Triggered the build and verified BUILD SUCCESS in console output.
Captured screenshot (see below).



Screenshots
Challenges and Solutions

Issue: Jenkins couldn’t access project files in the Docker container.
Solution: Used docker cp to copy hello-java-maven to /var/jenkins_home/workspace.


Issue: Maven not found in Jenkins.
Solution: Configured Maven 3.8.6 in Global Tool Configuration.



Learnings

Understood Jenkins Freestyle jobs and their role in CI/CD.
Learned how Maven compiles and packages Java code.
Gained experience with Dockerized Jenkins on EC2.
Improved debugging skills by analyzing console output.

Repository Structure
hello-java-maven/
├── src/main/java/HelloWorld.java
├── pom.xml
├── screenshots/
│   └── build-success.png
├── README.md
├── INTERVIEW.md

Why This Submission Stands Out

Hosted Jenkins in Docker on an AWS EC2 instance, showcasing cloud and container skills.
Provided detailed documentation with screenshots and debugging notes.
Organized Git commits to reflect a clear workflow.
Answered interview questions concisely in INTERVIEW.md to demonstrate understanding.

Best Intern Vibes: Crafted with care to impress!
