# CS-305: Summary of Analysis and Development for Artemis Financial

This repository was created to showcase concepts learned in CS-305 at Southern New Hampshire University.

##
### Briefly summarize your client, Artemis Financial, and their software requirements. Who was the client? What issue did they want you to address?
Artemis Financial is an investment and insurance firm that focuses on creating and managing financial itineraries tailored to its own clients’ needs. As the company is transitioning to a digital model, they enlisted our—Global Rain’s—services to fortify their application's network connectivity, check for and rectify vulnerabilities, and offer consultation regarding industry standard best practices for securing data at rest and in motion.   

##
### What did you do very well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?

I believe that my research into choosing appropriate algorithms for the application’s cryptographic cipher and hash function was potentially the strongest area of my work. This task also illuminated the fact that even the best cryptographic algorithms are only as effective as the weakest links of the code they’re implemented into. For example, if there are potential exploits within an application's input validation process, data is exploitable even before it reaches a cipher or hash function's input.

Regarding the benefit of software security to a company’s general well-being; it may be possible for a poorly protected company to exist for years without vulnerabilities being exploited. However, the potential consequences of those vulnerabilities being exploited may scale dramatically as the company grows. Additionally, higher-profile companies are often a bigger target for attackers, meaning that both the consequences and the chances of being attacked grow along with a company. This seems especially true in the financial domain. This is just one example of how software security can aid an enterprise from its establishment.  

#
### What part of the vulnerability assessment was challenging or helpful to you?

Understanding the reasons for "suppressing" vulnerabilities was very challenging for me. I still have a lot to learn about this concept. For the sake of security, it seems like even potential edge case vulnerabilities should be made known to developers. However, Iron-Clad Java—the textbook for CS-305—cautions about overwhelming developers with irrelevant warning flags. This will likely lead to all vulnerabilities ultimately being ignored, including relevant ones. To fully know which vulnerabilities should be ignored, one needs to have a comprehensive understanding of a code base, future development plans, and an extensive knowledge of Spring Boot and Maven. Overall, I believe this is a skill that needs to be fostered with time. 

Textbook referenced: Manico, Jim & Detlefsen, August. (2015). Iron-Clad Java : Building Secure Web Applications. McGraw Hill (Chapter 10)

#
### How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?

Measures taken to increase the layers of security for Artemis' application included analyzing input validation and potential authentication measures, transitioning deprecated HTTP routing to encrypted HTTPS routing, introducing secure cryptography algorithms for ciphers and hash functions, and analyzing/updating dependent libraries to mitigate their vulnerabilities. 

#
### How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?
Executing the application’s code to test that the Tomcat servlet started and routed my requests as expected allowed me to ensure that the application was functioning. Additionally, rebuilding the pom.xml file in Maven and browsing through the updated OWASP Dependency Check html document ensured that there were no new vulnerabilities resulting from the code refactoring. Reviewing the "Vulnerability Assessment Process Flow" graphic also helped me to consider areas to check for vulnerabilities that I may have missed on my own. 

#
### What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?
As mentioned in the previous response, the "Vulnerability Assessment Process Flow" graphic from my SNHU was helpful as a roadmap for understanding where to focus energy when checking for vulnerabilities. Other very useful resources included the OWASP Dependency Check application, the MvnRepository website, and the National Institute of Standards and Technology—NIST—website. I've bookmarked these resources for potential future use.

#
### Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?

The process of utilizing OWASP's Dependency Check was a central focus of my work for Artemis. In addition to building an awareness of common vulnerabilities and the skills to correct them, working with this tool also helps to foster experience in diagnosing, researching, updating, and finding workarounds for library/package issues not limited to the scope of this application, Maven, or even Spring Boot. These are essential skills for practically every development framework based on object-oriented programming. I believe that skills in this area are universally valuable to any employer involved in software development and/or filesystem management. 
