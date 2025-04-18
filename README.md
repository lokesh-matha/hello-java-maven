
# Hello Java Maven

## Project Overview
This project demonstrates the basic integration of **Java**, **Maven**, and **Jenkins** to build a simple Java application. The application prints "Hello, Jenkins + Maven!" to the console when executed.

This project serves as an introduction to Continuous Integration (CI) and Continuous Deployment (CD) using Jenkins.

## Project Structure

```
hello-java-maven/
├── src/
│   └── main/
│       └── java/
│           └── HelloWorld.java   # Main Java source file
├── pom.xml                      # Maven project configuration file
```

### Files:
- **HelloWorld.java**: A simple Java program that prints a message to the console.
- **pom.xml**: Maven build configuration file.

## Requirements

To run this project, you need the following tools:
- **Jenkins** (installed locally or via Docker)
- **Java JDK 8 or 11** 
- **Maven** (for building the project)
- **Git** (optional — if you choose to pull the repository from GitHub)

## Steps to Run Locally

### 1. Clone the repository (if using Git)
You can clone this repository to your local machine:

```bash
git clone https://github.com/your-username/hello-java-maven.git
cd hello-java-maven
```

### 2. Build the project with Maven
You can build the project using Maven from the command line:

```bash
mvn clean package
```

### 3. Run the Java Application
After building the project, you can run the Java application using:

```bash
java -jar target/hello-1.0.jar
```

This will print:

```
Hello, Jenkins + Maven!
```

## Jenkins Configuration

### 1. Start Jenkins (via Docker)
If you don't have Jenkins installed, you can start it with Docker using the following command:

```bash
docker run -p 8080:8080 jenkins/jenkins:lts
```

Access Jenkins at [http://localhost:8080](http://localhost:8080) in your browser.

### 2. Install Tools in Jenkins
Go to **Manage Jenkins → Global Tool Configuration**:

- Add **JDK** (JDK 8 or 11).
- Add **Maven** (e.g., Maven 3.8.6).

### 3. Create a Jenkins Freestyle Job
Go to **New Item** and create a **Freestyle project**.

In the **Build** section, select **Invoke top-level Maven targets**.

Set the **Goal** to `clean package` and save.

### 4. Run the Jenkins Job
Once the Jenkins job is configured, click **Build Now**. The console output should show:

```
[INFO] BUILD SUCCESS
```

This indicates that the project was successfully built and packaged.

## Conclusion
This project demonstrates a simple Java application built with Maven and integrated with Jenkins for continuous integration. The steps provided show how to build and run the project locally and through Jenkins.

Feel free to clone this project, modify it, and explore how Jenkins can help automate builds for Java applications.

---

### Instructions:
1. Replace `https://github.com/your-username/hello-java-maven.git` with the actual URL of your GitHub repository if you plan to use Git.
2. The README provides instructions for running the application locally and building it using Jenkins.

