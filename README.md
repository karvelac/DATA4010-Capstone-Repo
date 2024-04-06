# Utilizing Machine Learning Algorithms to Automate the Exam Grading Process
## Overview
Thie project uses machine learning to grade exams. The code shows representative examples of all work done to this end. It has examples of each type of the image classification models trained and tested, as well as a couple of representative examples of the different kinds of tests performed using Large Language Models (LLMs).

The following machine learning algorithms are performed in this file:
- K-Nearest Neighbor
- Support Vector Machine
- Convolutional Neural Network
- Large Language Model (ChatGPT)


## Goals
This project aims to accurately grade exams in an efficient and user-friendly way.

## Installation Instructions
In order to run the program, each of the listed Python libraries must be installed, if one is not installed, please run "pip install *library name* --upgrade" in your command prompt, or "conda install *library name* if using Anaconda.


## Data Preprocessing
The code also goes over the data-preprocessing steps which included:
- Separating the images into questions
- Resizing the images
- Importing image datasets
- Formatting the images
- Adjusting the target data to fit the truncated grading scheme

## How to Run
Before you run the program:

* Insert your valid OpenAI API key into the empty quotations located at the start of the **8) Model 4: LLMs** section, assigning it to the *client* variable
* Replace all file paths with the specific file paths on the system, as instructed by the comments

Each section is self-contained allowing users to run each test individually after proper data and library importing.

Section 1) will need the ranges and moduli adjusted for each exam. If there are no scanning errors then just one range, the length of the number of pages in the dataset needs to be looped. Additionally, if there are no issues the loop can be replaced by *for i in range(page_num_of_question, num_pages_in_dataset + 1, num_pages_per_booklet)* which will also remove the need for the modulo operation. The method provided works best for when there are scanning issues, as it allows one to not have to find the exact page of the scanning issue, but simply just the booklet it occurs in. If this task has not yet been performed (i.e. the questions have not been separated yet) and the tests are all performed on the same dataset, the entire program can be run from start to finish, assuming all file paths and the API code have been updated. If the questions have been separated and the previous conditions otherwise met, then the entire program from section 2) onward can be run. Section 1) can only be run **once** without first moving the images back to the source folder from the destination one.

## Results
All results were measured using accuracy (proportion of exams correctly graded). The LLMs performed very well on the truncated grading scheme, whereas the image classification models performed poorly.

## Acknowledgements
I duly acknowledge the developers of all the libraries used in this project.



