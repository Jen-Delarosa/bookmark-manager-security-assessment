# bookmark-manager-security-assesment

## Project Overview

A security assessment was performed on the Badly Coded Bookmark Manager(bcbm). Bcbm is a web browser that allows the user to add URLs to their bookmark manager for easy access. Users can also rank their bookmarks and can sign into their cloud account. Cloud is used for users to access their bookmark manager from different devices by logging into their account.   

Using the STRIDE threat model as a basis for security goals, I analyzed the system for security weaknesses and evaluated how user data, authentication codes, and bookmarks were stored and managed. The security assessment was done within a virtual machine to simulate attacks on the system to determine the presence of vulnerabilities. These attacks were simulated by writing proof-of-concept scripts to run against the code.
 
The findings from the security assessment revealed a total of four vulnerabilities. A denial-of-service vulnerability was found when a user ranked a bookmark with a number greater than ten. This is a denial-of-service vulnerability because, as a result, the user’s bookmark manager crashes, and they can no longer add bookmarks or visit old bookmarks. More information about the vulnerabilities found is in the project-report.pdf within the report directory. 

The vulnerability directory contains four proof-of-concept scripts to showcase the vulnerabilities in action. A README.md file is provided in this directory to explain how to run the scripts and expected results. However, the bcbm system code was not provided in this repository because it was not written by me. The report titled project-report.pdf and vulnerability proof-of-concept scripts were written by me and are located in this repository.  

For a more in-depth explanation of the bcbm system design, the threat model used for security goals, and a summary of findings, please refer to the project-report.pdf within the report directory. 



