# Task 8: Interview Questions and Answers

Below are the answers to the interview questions for Task 8, demonstrating an understanding of Jenkins and Maven.

1. **What is Jenkins?**
- Jenkins is an open-source automation server used for continuous integration and continuous deployment (CI/CD). It automates building, testing, and deploying software, allowing developers to integrate code changes frequently and reliably.

2. **How do you create a Jenkins job?**
- To create a Jenkins job:
   - Go to the Jenkins dashboard and click “New Item.”
   - Enter a name, select “Freestyle project,” and click “OK.”
   - Configure source code management, build triggers, and build steps (e.g., Invoke Maven targets).
   - Save and trigger the build manually or via a trigger.

3. **What is Maven used for?**
- Maven is a build automation tool primarily for Java projects. It simplifies and standardizes the build process by providing a uniform build system, dependency management, and a central repository for libraries.

4. **How does Jenkins use build tools like Maven?**
Jenkins integrates with Maven via plugins or direct commands. In a Freestyle job, you can specify Maven goals (e.g., `clean package`) and point to a `pom.xml` file. Jenkins executes the Maven build and captures the output.

5. **What is the difference between compile and package in Maven?**
   - `compile`: Compiles the source code into bytecode, producing `.class` files in the `target/classes` directory.
   - `package`: Compiles the code, runs tests, and packages the compiled code into a distributable format (e.g., `.jar` or `.war`) in the `target` directory.

6. **Where do you configure tools in Jenkins?**
- Tools like Maven are configured in `Manage Jenkins` > `Global Tool Configuration`. You can add and specify versions for tools like JDK, Maven, or Git, which Jenkins uses during builds.

7. **How do you debug a failed Jenkins build?**
   - Check the **Console Output** for error messages or stack traces.
   - Verify the `pom.xml` file and project structure.
   - Ensure tools (e.g., Maven, JDK) are correctly configured in Jenkins.
   - Test the build locally using `mvn clean package` to isolate issues.
   - Review Jenkins logs (`/var/jenkins_home/logs`) for system-level errors.
