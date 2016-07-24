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

4. Suppose that the C programming language is chosen in the project in exercise 2. Recommend a detailed code review checklist to the review team.

5. In addition to code review, what other static unit testing techniques would you recommend for the project in exercise 3? Justify your answer.

6. Describe the special role of a recordkeeper.
	- Recordkeeper creates a summary of the meeting. A list of all the CRs, the dates of which will be fixed, and the persons respnsible for validating the CRs. 
 	  Then it will be distributed to all the members of the group. The author will document the improvements made to the code in CRs.

7. Discuss the importance of code review rework and validation.
	- rework and validation is important because after summarizing all the documents of the CRs, then this will determine if there are defects 
	  during validation process and ensuring that the suggested improvements have been implemented correctly.
