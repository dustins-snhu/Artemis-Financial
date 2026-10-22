CS 305: Software Security
Artemis Financial Secure Software Project
This repository contains my work for the CS 305 Software Security course project. The project focused on evaluating an existing Java application for security concerns and applying secure software development practices without disrupting the application's existing functionality.

Client and Project Requirements
Artemis Financial is a financial services company that required improvements to the security of its existing software application. The primary objective was to identify potential software security vulnerabilities and improve the application's security through cryptography, secure communications, vulnerability assessment, and testing.

The project required evaluating the existing application, implementing a cryptographic hash function, generating a certificate for secure communications, converting the application from HTTP to HTTPS, and performing additional security testing after the application was refactored.

Software Security and Vulnerability Assessment
One area I believe I handled particularly well was separating the different types of security concerns within the application. Rather than treating "security" as a single problem, I considered cryptography, communications, application logic, and third-party dependencies independently and then applied controls appropriate to each area.

Secure coding is important because software vulnerabilities can compromise the confidentiality, integrity, and availability of information. This is especially important for financial applications, where the software may be responsible for processing sensitive business and customer information. Strong software security also benefits the overall organization by reducing avoidable risk and making security part of the development process rather than something addressed only after software is deployed.

One of the most useful parts of the vulnerability assessment was learning the distinction between different forms of security analysis. For example, OWASP Dependency-Check is valuable for identifying dependencies associated with known CVEs, but dependency analysis does not replace manual review of application-specific source code. Understanding the purpose and limitations of individual security tools was one of the more valuable lessons from the project.

Layered Security
I increased the security of the application through multiple layers. I implemented SHA-256 hashing to provide data-integrity verification, generated a certificate and cryptographic key pair using Java Keytool, and configured the Spring Boot application to communicate through HTTPS. These controls address different security requirements rather than relying on a single mechanism to protect the entire application.

In future software projects, I would continue using a combination of automated dependency analysis, manual code review, functional testing, and established security and cryptographic standards. Mitigation techniques should be selected based on the type and severity of the vulnerability rather than applying the same solution to every security problem.

Testing and Verification
I verified the refactored application by compiling and executing the code and then testing its functionality. I confirmed that the application could generate the expected SHA-256 checksum and that the Spring Boot server successfully operated through HTTPS on port 8443. I also manually reviewed the refactored code for syntactical, logical, and security problems.

After completing the refactoring, I performed another OWASP Dependency-Check scan to examine the application's third-party dependencies for known vulnerabilities. I treated dependency scanning and application testing as complementary activities. Dependency-Check provided information about known vulnerabilities associated with external components, while functional testing and manual code review were used to evaluate the behavior and implementation of the code itself.

Tools and Secure Coding Practices
Tools, technologies, and practices used during this project included:

Java
Spring Boot
Maven
SHA-256 cryptographic hashing
Java MessageDigest
Java Keytool
RSA public/private key cryptography
PKCS12 keystores and certificates
HTTPS/TLS
OWASP Dependency-Check
Manual secure code review
Functional and regression testing
Layered security and defense-in-depth
One practice I will carry into future projects is using established and tested cryptographic implementations instead of attempting to create custom cryptographic solutions. I also gained practical experience distinguishing vulnerabilities in application code from vulnerabilities associated with third-party software dependencies.

Portfolio Reflection
For a future employer, I would use this project to demonstrate my ability to approach an existing software system from both a development and security perspective. The project demonstrates that I can examine an existing codebase, identify different categories of security risk, implement appropriate security controls, and verify that the software remains functional after refactoring.

My completed Artemis Financial Practices for Secure Software Report provides additional documentation of this work, including cryptographic hashing, certificate generation, HTTPS configuration, dependency analysis, and functional security testing. Along with the refactored source code, the project demonstrates my ability to incorporate software security into the development lifecycle instead of treating security as a separate concern after development is complete.