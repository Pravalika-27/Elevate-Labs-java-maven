# Task 8: Java Maven Build with Jenkins on AWS EC2

This repository contains the deliverables for Task 8 of the DevOps Internship, demonstrating a Java Maven build job in Jenkins on an AWS EC2 Ubuntu instance.

## Objective
Build a simple Java HelloWorld app using Maven in a Jenkins Freestyle job, hosted on an EC2 instance.

## Tools Used
- AWS EC2 (Ubuntu 22.04, t2.micro)
- Jenkins (via Docker)
- Java JDK 11
- Maven 3.8.6
- Git

## Steps
1. Launched an EC2 Ubuntu instance with ports 22, 80, and 8080 open.
2. Installed Java, Maven, Docker, and Git.
3. Set up Jenkins in a Docker container.
4. Created a Java HelloWorld app with `pom.xml`.
5. Configured a Jenkins Freestyle job to build the app with Maven (`clean package`).
6. Captured a screenshot of the successful build console output.
7. Documented the process and interview questions.

## Challenges and Learnings
- **Challenge**: Ensuring Jenkins could access the project files in the Docker container.
- **Solution**: Copied files to the Jenkins workspace using `docker cp`.
- **Learning**: Understood how Jenkins integrates with Maven and the importance of console output for debugging.

## Interview Questions
See [INTERVIEW.md](INTERVIEW.md) for answers to the task’s interview questions.

## How to Replicate
Follow the steps in this README or refer to the detailed guide in the repository root.

*Best Intern Touch*: This submission is crafted with precision to demonstrate DevOps skills and a commitment to excellence!
