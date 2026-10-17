# CS 305 – Software Security

Brian Minor 
Southern New Hampshire University  
Bachelor of Science in Computer Science

## Project Overview

This repository contains my work from CS 305: Software Security at Southern New Hampshire University. For this course, I worked with a Java Spring Boot application for a fictional financial consulting company called Artemis Financial. The main goal was to identify potential security vulnerabilities and improve the application's security through encryption, secure communication, and code testing.

The artifact I selected for my portfolio is my **Artemis Financial Practices for Secure Software Report** from Project Two. This report documents the security improvements I implemented, the tools I used, and the testing I performed to verify that the application continued functioning correctly.

## 1. Client and Software Requirements

Artemis Financial is a financial consulting company that provides individualized financial planning services to its customers. Because the company handles sensitive financial information, protecting customer data is an important part of its operations.

The company wanted to improve the security of its existing software application by identifying vulnerabilities and implementing stronger security measures. My responsibility was to review the application, determine what security improvements were needed, and refactor the code to support secure communication and data integrity.

## 2. Software Security and Vulnerability Assessment

One thing I did well during this project was working through the vulnerability assessment process and identifying potential security concerns within the application. I used OWASP Dependency-Check to scan the project's dependencies and identify libraries with known vulnerabilities. I also reviewed the application code and configuration files to better understand how the software handled security.

I learned that secure coding involves more than just making sure a program works. An application can function correctly while still containing vulnerabilities that could be exploited. Writing secure code helps protect sensitive information, prevent unauthorized access, and reduce the chances of a security breach.

For a financial company like Artemis Financial, software security also helps maintain customer trust. A security incident could result in financial losses, damaged reputation, and interruptions to business operations. Taking security seriously helps protect both the company and its customers.

## 3. Challenges During the Vulnerability Assessment

One of the more challenging parts of this project was working with OWASP Dependency-Check and understanding the results. The reports identified multiple vulnerabilities in older dependencies, and I had to spend time reviewing the findings to understand what they meant.

Another challenge was configuring HTTPS for the Spring Boot application. I generated a self-signed certificate using Java Keytool and configured the application to use a PKCS12 keystore. Getting the application to start correctly required checking the configuration settings and troubleshooting issues with the server port.

Although these steps were frustrating at times, they helped me become more comfortable reading error messages, working with security tools, and troubleshooting Java applications.

## 4. Increasing Layers of Security

I improved the application's security by implementing multiple security measures.

First, I configured HTTPS using a self-signed certificate so that communication between the application and the browser could be encrypted. I generated a 3072-bit RSA certificate using Java Keytool and configured Spring Boot to use the certificate through a PKCS12 keystore.

I also implemented SHA-256 hashing using Java's MessageDigest class. The application generates a checksum from a predefined string, demonstrating how hashing can be used to detect changes to data when compared against a trusted checksum.

These changes addressed different security concerns. HTTPS protects information while it travels between systems, while hashing provides a way to check data integrity.

In future projects, I would continue using OWASP Dependency-Check, manual code reviews, and additional security testing tools to identify vulnerabilities. I would also consider the severity of each vulnerability, its potential impact, and whether the affected component is actually used before deciding which mitigation techniques to implement.

## 5. Testing Application Functionality and Security

After refactoring the application, I tested it to make sure the changes worked correctly and did not prevent the software from running.

I used Maven to build the project and confirmed that the build completed successfully. I then ran the Spring Boot application through Eclipse and verified that it was running over HTTPS on port 8443.

I also tested the /hash endpoint in my browser to confirm that the application generated and displayed the expected SHA-256 checksum.

To check for potential security issues, I reviewed the updated code and configuration files and ran OWASP Dependency-Check again. I also compared the application's dependencies before and after making changes.

The scan continued to identify vulnerabilities in several older libraries included with the original project. Although I did not add new third-party application dependencies, the existing vulnerabilities would still need to be addressed before the software could be considered ready for production.

This experience showed me that a successful build does not necessarily mean an application is secure. Functional testing and security testing are both important parts of software development.

## 6. Resources, Tools, and Coding Practices

Throughout this project, I worked with several tools and technologies that I expect to use again in future programming assignments and professional IT work.

- **Java:** Used to implement the SHA-256 checksum functionality.
- **Eclipse IDE:** Used to review, modify, and test the application.
- **Spring Boot:** Used to configure and run the web application.
- **Maven:** Used to manage dependencies and build the project.
- **OWASP Dependency-Check:** Used to identify known vulnerabilities in third-party libraries.
- **Java Keytool:** Used to generate the self-signed certificate and configure the keystore.
- **SHA-256:** Used to demonstrate cryptographic hashing and data integrity.
- **HTTPS/TLS:** Used to establish encrypted communication between the application and browser.

One of the biggest lessons I learned was the importance of testing changes as I make them instead of waiting until the end of a project. Reading console output, checking configuration files, and documenting my work made troubleshooting much easier.

I also learned that using built-in Java security libraries when appropriate can help avoid introducing unnecessary third-party dependencies.

## 7. Portfolio Reflection and Future Career

This project gave me a better understanding of how software security is applied to an actual application. Before taking this course, I understood the importance of protecting information, but I had less experience implementing security features directly in Java.

Through this project, I gained experience generating certificates, configuring HTTPS, implementing cryptographic hashing, reviewing dependencies, and testing an application after making security-related changes.

If I were showing this project to a future employer, I would highlight my Practices for Secure Software Report, the HTTPS configuration, the SHA-256 implementation, and the vulnerability assessment results. These demonstrate my ability to identify potential problems, research solutions, make changes to existing software, and verify that those changes work correctly.

As I continue working toward my bachelor's degree in computer science, I want to keep improving my programming and troubleshooting skills. This project reinforced how important security is throughout the development process and gave me practical experience that I can build on in future projects.

## Project Artifact

**Artemis Financial – Practices for Secure Software Report**

File: CS305_Project_Two_Brian_Minor.docx

The report includes documentation of the security improvements, certificate generation, HTTPS configuration, checksum implementation, vulnerability scanning, and functional testing completed during Project Two.

**Note:** The application was developed and tested in a classroom environment. The self-signed certificate and remaining dependency vulnerabilities would need to be addressed before production deployment. No private keys or keystore passwords are included in this public portfolio.
