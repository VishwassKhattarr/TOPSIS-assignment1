# TOPSIS Assignment
Name: Vishwas Khattar
Roll Number: 102303170

This repository contains the complete implementation of the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method as part of Assignment 1. The assignment is divided into three parts. In Part 1, a command line based TOPSIS program is implemented. In Part 2, the same program is converted into a Python package and published on PyPI. In Part 3, a web-based TOPSIS service is developed and deployed.

The objective of this assignment is to understand multi-criteria decision making using TOPSIS and to implement it across different platforms including command line, Python package distribution, and a web application.


PART 1: Command Line Based TOPSIS Program

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
Incorrect number of command line arguments
Missing input file
Non-numeric values in criteria columns
Mismatch between number of weights, impacts, and criteria
Invalid impact symbols (only + or - allowed)

Example usage of the program is provided in the assignment and the output file contains two additional columns: TOPSIS Score and Rank.
<img width="794" height="438" alt="image" src="https://github.com/user-attachments/assets/fe6793d6-3125-4f94-8217-76809b89fd53" />

Invalid impact symbols (only + or - allowed)
Example usage of the program is provided in the assignment and the output file contains two additional columns: TOPSIS Score and Rank.
Writes the result to an output CSV file.
