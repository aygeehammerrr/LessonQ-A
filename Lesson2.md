1. Study the Yourdon [2] concept of a design walkthrough and the IBM concept [1] of a design inspection. Discuss the similarities and the differences between them. 
   Differences:
	- A walkthrough is an informal version of inspection. There is no preparation required for this and there is no checklist used. 
	  Whereas inspection is a more formal process than a walkthrough. It is used to collect metrics and statistics about the software process. 
          It is a formalized method in which it follows standards and requirements. 
   Similarities:
	- Both are used in static testing

2. A software engineering group is developing a mission-critical software system that will launch laser-guided missiles to its destinations. This is a new kind of product that was never built by the company. 
   As a quality assurance manager, which code review methodology—walkthrough or inspection—would you recommend? Justify your answer.
	- Since it is a mission-critical software system, I would recommend to use the inspection methodology. It needs longer time to carefully analyze its process because it is a laser-guided missile. 
	  If anything goes wrong in the program of the missile, then it can lead to disaster, going to another destination instead of its original destination.

3. What size of a review team would you recommend for the project in exercise 2, and why? What are the different roles of each member of the review team? What groups should send representatives to participate in code review?	
	- The project being a mission-critical software will definitely involve a lot of members in a review team because it is a crucial project that can affect lives. The team must consist of people with expertise in different fields especially ballistics, and also those who are skilled in code review. These people will act as key persons in making the software free from any possible failures that may cause damage or loss of life. They will also be the ones who should verify if the software follows the required specifications. The ministry of defense is the most important group to spearhead the review since the software is aligned to them.

4. Suppose that the C programming language is chosen in the project in exercise 2. Recommend a detailed code review checklist to the review team.
	-	1. Code formatting

		While going through the code, check the code formatting to improve readability and ensure that there are no blockers:
		
		a) Use alignments (left margin), proper white space. Also ensure that code block starting point and ending point are easily identifiable.
		
		b) Ensure that proper naming conventions (Pascal, CamelCase etc.) have been followed. 
		
		c) Code should fit in the standard 14 inch laptop screen.  There shouldn’t be a need to scroll horizontally to view the code. In a 21 inch monitor, other windows (toolbox, properties etc.) can be opened while modifying code, so always write code keeping in view a 14 inch monitor.
		
		d) Remove the commented code as this is always a blocker, while going through the code. Commented code can be obtained from Source Control (like SVN), if required.
		
		2. Architecture
		
		a) The code should follow the defined architecture.
		
		Separation of Concerns followed
		Split into multiple layers and tiers as per requirements (Presentation, Business and Data layers).
		Split into respective files (HTML, JavaScript and CSS).
		Code is in sync with existing code patterns/technologies.
		Design patterns: Use appropriate design pattern (if it helps), after completely understanding the problem and context.
		3. Coding best practices
		
		No hard coding, use constants/configuration values.
		Group similar values under an enumeration (enum).
		Comments – Do not write comments for what you are doing, instead write comments on why you are doing. Specify about any hacks, workaround and temporary fixes. Additionally, mention pending tasks in your to-do comments, which can be tracked easily.
		Avoid multiple if/else blocks.
		Use framework features, wherever possible instead of writing custom code.
		4. Non Functional requirements
		
		a) Maintainability (Supportability) – The application should require the least amount of effort to support in near future. It should be easy to identify and fix a defect.
		
		Readability: Code should be self-explanatory. Get a feel of story reading, while going through the code. Use appropriate name for variables, functions and classes. If you are taking more time to understand the code, then either code needs refactoring or at least comments have to be written to make it clear.
		Testability: The code should be easy to test. Refactor into a separate function (if required). Use interfaces while talking to other layers, as interfaces can be mocked easily. Try to avoid static functions, singleton classes as these are not easily testable by mocks.
		Debuggability: Provide support to log the flow of control, parameter data and exception details to find the root cause easily. If you are using Log4Net like component then add support for database logging also, as querying the log table is easy.
		Configurability: Keep the configurable values in place (XML file, database table) so that no code changes are required, if the data is changed frequently.
		b) Reusability
		
		DRY (Do not Repeat Yourself) principle: The same code should not be repeated more than twice.
		Consider reusable services, functions and components.
		Consider generic functions and classes.
		c) Reliability – Exception handling and cleanup (dispose) resources.
		
		d) Extensibility – Easy to add enhancements with minimal changes to the existing code. One component should be easily replaceable by a better component.
		
		e) Security – Authentication, authorization, input data validation against security threats such as SQL injections and Cross Site Scripting (XSS), encrypting the sensitive data (passwords, credit card information etc.)
		
		f) Performance
		
		Use a data type that best suits the needs such as StringBuilder, generic collection classes.
		Lazy loading, asynchronous and parallel processing.
		Caching and session/application data.
		g) Scalability – Consider if it supports a large user base/data? Can this be deployed into web farms?
		
		h) Usability – Put yourself in the shoes of a end-user and ascertain, if the user interface/API is easy to understand and use. If you are not convinced with the user interface design, then start discussing your ideas with the business analyst.
		
		5. Object-Oriented Analysis and Design (OOAD) Principles
		
		Single Responsibility Principle (SRS): Do not place more than one responsibility into a single class or function, refactor into separate classes and functions.
		Open Closed Principle: While adding new functionality, existing code should not be modified. New functionality should be written in new classes and functions.
		Liskov substitutability principle: The child class should not change the behavior (meaning) of the parent class. The child class can be used as a substitute for a base class.
		Interface segregation: Do not create lengthy interfaces, instead split them into smaller interfaces based on the functionality. The interface should not contain any dependencies (parameters), which are not required for the expected functionality.
		Dependency Injection: Do not hardcode the dependencies, instead inject them.
		In most cases the principles are interrelated, following one principle automatically satisfies other principles. For e.g: if the ‘Single Responsibility Principle’ is followed, then Reusability and Testability will automatically increase.
		
		In a few cases, one requirement may contradict with other requirement. So need to trade-off based on the importance of the weight-age, e.g. Performance vs Security. Too many checks and logging at multiple layers (UI, Middle tier, Database) would decrease the performance of an application. But few applications, especially relating to finance and banking require multiple checks, audit logging etc. So it is ok to compromise a little on performance to provide enhanced security.


5. In addition to code review, what other static unit testing techniques would you recommend for the project in exercise 3? Justify your answer.
	- The software being a mission-critical type needs actual simulation since it is the best way to test if any failure will occur. Although it will be quite expensive, doing this test will allow the developing team to pinpoint where the software went wrong.

6. Describe the special role of a recordkeeper.
	- Recordkeeper creates a summary of the meeting. A list of all the CRs, the dates of which will be fixed, and the persons respnsible for validating the CRs. 
 	  Then it will be distributed to all the members of the group. The author will document the improvements made to the code in CRs.

7. Discuss the importance of code review rework and validation.
	- rework and validation is important because after summarizing all the documents of the CRs, then this will determine if there are defects 
	  during validation process and ensuring that the suggested improvements have been implemented correctly.
