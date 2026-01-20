#TOPSIS Assignment


Name: Vishwas Khattar


Roll Number: 102303170


This repository contains the complete implementation of the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method as part of Assignment 1. The assignment is divided into three parts. In Part 1, a command line based TOPSIS program is implemented. In Part 2, the same program is converted into a Python package and published on PyPI. In Part 3, a web-based TOPSIS service is developed and deployed.

The objective of this assignment is to understand multi-criteria decision making using TOPSIS and to implement it across different platforms including command line, Python package distribution, and a web application.


**PART 1: Command Line Based TOPSIS Program**

In Part 1, the TOPSIS algorithm is implemented in Python as a command line program. The program takes a CSV file as input along with weights and impacts for each criterion and produces a ranked output using the TOPSIS method.

The input file must contain at least three columns. The first column contains alternatives (for example, names of phones or funds) and the remaining columns contain numeric values representing different criteria.

The program performs the following steps:


1.Reads the input CSV file.


2.Validates the number of columns, weights, and impacts.


3.Normalizes the data using vector normalization.


4.Applies weights to the normalized data.


5.Calculates the ideal best and ideal worst solutions.


6.Computes the distance of each alternative from the ideal best and worst.


7.Calculates the TOPSIS score.


8.Ranks the alternatives based on the TOPSIS score.


9.Writes the result to an output CSV file.




The program includes proper error handling for:


- Incorrect number of command line arguments


- Missing input file


- Non-numeric values in criteria columns


- Mismatch between number of weights, impacts, and criteria


- Invalid impact symbols (only + or - allowed)

- Example usage of the program is provided in the assignment and the output file contains two additional columns: TOPSIS Score and Rank.


<img width="1067" height="261" alt="image" src="https://github.com/user-attachments/assets/41b4c1bf-7711-4ab9-989d-c5ac85c58824" />



Invalid impact symbols (only + or - allowed)
Example usage of the program is provided in the assignment and the output file contains two additional columns: TOPSIS Score and Rank.
Writes the result to an output CSV file.





**PART 2: Python Package and PyPI Publishing**

In Part 2, the TOPSIS command line program is converted into a reusable Python package. The package is structured properly with setup files and metadata so that it can be installed using pip.


The package allows users to install and use the TOPSIS functionality directly from the command line after installation. This part demonstrates understanding of Python packaging, dependency management, and distribution.


The package is published on PyPI following the required naming convention specified in the assignment. After installation, users can run the TOPSIS program in the same way as in Part 1 but without manually managing the script file.


This part shows how a standalone Python script can be converted into a distributable package that can be used by others.


link:https://pypi.org/project/Topsis-VishwasKhattar-102303170/


command:pip install Topsis-VishwasKhattar-102303170


**PART 3: Web Service for TOPSIS**

In Part 3, a web-based TOPSIS service is developed using the Flask framework. This web application provides a user-friendly interface to perform TOPSIS analysis without using the command line.



The web application allows the user to:




- Upload an input CSV file


- Enter weights for each criterion


- Enter impacts for each criterion


- Provide an email ID to receive the result




Once the form is submitted:




The input data is validated.


The TOPSIS algorithm is applied using the same logic as Part 1.


The result is displayed on the website.


The output CSV file is sent to the user via email as an attachment.



The web application uses HTML and CSS for the frontend and Flask for backend processing. Email functionality is implemented using SMTP with proper authentication.



**note- the SMTP free version is blocked on deployment services such as render, the functionality will be updated using some other mail service protocol.**

The application is deployed online using Render so that it can be accessed publicly.

Live Web Application Link:


Link:https://topsis-web-service-a3y5.onrender.com



working screenshots:



1.Initial Landing Page


<img width="1919" height="970" alt="image" src="https://github.com/user-attachments/assets/e20e3266-0216-4905-817f-ffcc931c49da" />



<img width="1918" height="970" alt="image" src="https://github.com/user-attachments/assets/ebab6697-1175-4867-a551-1dac7cd301ab" />



2.Results after clicking Run TOPSIS button


<img width="1918" height="971" alt="image" src="https://github.com/user-attachments/assets/406cfbd8-39af-4934-8722-d1fa60233080" />


--result attached and sent via email
<img width="1919" height="912" alt="image" src="https://github.com/user-attachments/assets/ea15a6b1-4043-4f19-8299-8443b2276d1a" />




**Note on deployment delay**
*The web application is deployed using Render’s free service. When the deployed link is opened after a period of inactivity, it may take around 30 to 60 seconds to respond initially, and also takes time to respond once run TOPSIS button is clicked. This happens because free Render services automatically go into a sleep state when not in use. Once the service wakes up, the application functions normally. For production-level or continuous usage, the application can be deployed on better alternatives such as Railway, AWS EC2, or Google Cloud Run, which do not have cold start delays and provide more reliable performance.*
