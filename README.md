TOPSIS Assignment
=================

**Name:** Vishwas Khattar  
**Roll Number:** 102303170  

---

This repository contains the complete implementation of the **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** method as part of **Assignment 1**.

The assignment is divided into **three parts**:

• Command Line TOPSIS Program under file named topsis.py
• Python Package and PyPI Publishing under file named PyPi/Topsis-VishwasKhattar-102303170 
• Web-based TOPSIS Service under file named topsis-web-service

The objective of this assignment is to understand **multi-criteria decision making using TOPSIS** and to implement it across different platforms including **command line tools, Python package distribution, and a web application**.

---

PART 1: Command Line Based TOPSIS Program
----------------------------------------

In **Part 1**, the TOPSIS algorithm is implemented in **Python** as a command line program.

The program takes a CSV file as input along with weights and impacts for each criterion and produces a ranked output using the TOPSIS method.

### Input File Requirements

• The input file must contain **at least three columns**  
• The **first column** contains alternatives (e.g., phone names, funds, etc.)  
• Remaining columns must contain **numeric values** representing criteria  

### Steps Performed by the Program

1. Reads the input CSV file  
2. Validates the number of columns, weights, and impacts  
3. Normalizes the data using vector normalization  
4. Applies weights to the normalized data  
5. Calculates the ideal best and ideal worst solutions  
6. Computes the distance from ideal best and ideal worst  
7. Calculates the TOPSIS score  
8. Ranks the alternatives based on the TOPSIS score  
9. Writes the result to an output CSV file  

### Error Handling Included

• Incorrect number of command line arguments  
• Missing input file  
• Non-numeric values in criteria columns  
• Mismatch between number of weights, impacts, and criteria  
• Invalid impact symbols (only `+` or `-` allowed)  

The output CSV file contains two additional columns:

• **TOPSIS Score**  
• **Rank**

### Example Output Screenshot

<img width="1067" height="261" alt="Command Line Output" src="https://github.com/user-attachments/assets/41b4c1bf-7711-4ab9-989d-c5ac85c58824" />

### Methodology

 
 The following methodology is implemented in this project:
 

♦ The program accepts four command-line inputs: the input CSV file, a list of weights, a list of impacts, and the output CSV file. If the number of arguments is incorrect, the program terminates with an error message.

♦ The input CSV file is validated to ensure that it exists and can be read successfully. The file must contain at least three columns, where the first column represents the alternatives and the remaining columns represent numerical criteria.

♦ All criteria columns (from the second column onwards) are checked to ensure they contain only numeric values. If any non-numeric value is found, execution is stopped with an appropriate error.

♦ The weights and impacts are extracted from the command-line input and split using commas. The number of weights and impacts is validated to ensure it matches the number of criteria columns.

♦ Weights are converted to floating-point numbers. Impacts are validated to ensure that each impact is either a plus (+) or minus (−), representing benefit and cost criteria respectively.

♦ The decision matrix is normalized using vector normalization. Each value in a column is divided by the square root of the sum of squares of that column. This ensures that all criteria are brought to a comparable scale.

♦ The normalized matrix is multiplied by the corresponding weights to obtain the weighted normalized decision matrix.

♦ The ideal best and ideal worst solutions are determined for each criterion. For benefit criteria (+), the maximum value is considered ideal best and the minimum value as ideal worst. For cost criteria (−), the minimum value is considered ideal best and the maximum value as ideal worst.

♦ The Euclidean distance of each alternative from the ideal best and ideal worst solutions is calculated using the weighted normalized matrix.

♦ The TOPSIS score for each alternative is computed as the ratio of its distance from the ideal worst to the sum of its distances from the ideal best and ideal worst.

♦ Alternatives are ranked in descending order of their TOPSIS scores. A higher score indicates closer proximity to the ideal solution and therefore a better rank.

♦ The final output, including the TOPSIS score and rank, is written to the specified output CSV file.

This methodology ensures an objective and systematic evaluation of alternatives based on multiple conflicting criteria.


---

PART 2: Python Package and PyPI Publishing
-----------------------------------------

In **Part 2**, the command line TOPSIS program is converted into a **reusable Python package**.

The package is structured properly with setup files and metadata so that it can be installed using **pip**.

### Installation Command

pip install Topsis-VishwasKhattar-102303170


### PyPI Link

https://pypi.org/project/Topsis-VishwasKhattar-102303170/

After installation, users can run the TOPSIS program in the same way as Part 1, without manually managing the script file.

This part demonstrates understanding of:

• Python packaging  
• Dependency management  
• Package distribution using PyPI  

---

PART 3: Web Service for TOPSIS
------------------------------

In **Part 3**, a **web-based TOPSIS service** is developed using the **Flask framework**.

The web application provides a user-friendly interface to perform TOPSIS analysis without using the command line.

### Features of the Web Application

• Upload an input CSV file  
• Enter weights for each criterion  
• Enter impacts for each criterion  
• Provide an email ID to receive the result  

### Workflow After Submission

1. Input data is validated  
2. TOPSIS algorithm is applied using the same logic as Part 1  
3. Results are displayed on the website  
4. Output CSV file is sent to the user via email  

The frontend is built using **HTML and CSS**, and backend processing is handled using **Flask**.

Email functionality is implemented using **SMTP with authentication**.

**Note:**  
The SMTP free version is blocked on deployment services such as Render.  
This functionality will be updated using an alternative mail service protocol.

---

Live Web Application
--------------------

https://topsis-web-service-a3y5.onrender.com

---

Working Screenshots
-------------------

### 1. Initial Landing Page

<img width="1919" height="970" alt="Landing Page 1" src="https://github.com/user-attachments/assets/e20e3266-0216-4905-817f-ffcc931c49da" />

<img width="1918" height="970" alt="Landing Page 2" src="https://github.com/user-attachments/assets/ebab6697-1175-4867-a551-1dac7cd301ab" />

### 2. Results After Clicking “Run TOPSIS”

<img width="1918" height="971" alt="Results Page" src="https://github.com/user-attachments/assets/406cfbd8-39af-4934-8722-d1fa60233080" />

### 3. Result Sent via Email

<img width="1919" height="912" alt="Email Result" src="https://github.com/user-attachments/assets/ea15a6b1-4043-4f19-8299-8443b2276d1a" />

---

Note on Deployment Delay
-----------------------

The web application is deployed using **Render’s free service**.

When the deployed link is opened after a period of inactivity:

• Initial response may take **30–60 seconds**  
• Clicking the **Run TOPSIS** button may also take time  

This happens because free Render services go into a **sleep state** when not in use.

Once the service wakes up, the application functions normally.

For production-level or continuous usage, the application can be deployed on:

• Railway  
• AWS EC2  
• Google Cloud Run  

These platforms avoid cold start delays and provide better reliability.

---

End of README
