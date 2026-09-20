# CALO_PA-4

## This repository focuses on data wrangling and data visualization using Python and Pandas. It involves filtering variables needed for our Programming Assignment 4 in ECE2112

I. Intended Learning Outcomes
At the end of this laboratory activity, the student should be able to:
1. filter tabular data using several categorical and numerical conditions;
2. construct focused DataFrames by selecting relevant features;
3. summarize the relationship between categorical features and a numerical variable; and
4. communicate a data comparison using clear and correctly labeled plots.

# PROBLEM A: VISAYAS COMMUNICATION DATAFRAME
Create a DataFrame named VisComm containing students whose Hometown is Visayas and whose Track
is Communication. 

## CODE
<img width="1503" height="665" alt="image" src="https://github.com/user-attachments/assets/f51b26f0-27cd-46f7-836d-c5dffd2861c5" />

## EXPLANATION
This code loads the dataset and extracts a targeted subset of student records according to specific criteria. It first strips accidental whitespace from all 
column names and ensures an 'Average' score exists by calculating the row-wise mean of available subject exam columns if the column is not already present. 
It then applies a compound boolean condition to filter for students whose 'Hometown' is 'Visayas' and whose 'Track' is 'Communication', retaining only 
the 'Name', 'Gender', 'Math', 'Electronics', and 'Average' columns in the new VisComm DataFrame. Finally, it displays the resulting five-row DataFrame along with 
its total row count.   


# PROBLEM B: VISAYAS FEMALE DATAFRAME

## CODE

<img width="1193" height="761" alt="image" src="https://github.com/user-attachments/assets/c40de59b-5cb1-4bd7-a6d8-92cb73a83a4d" />

## EXPLANATION
This code filters the dataset to focus on female examinees from Visayas and evaluates their performance. It first checks if the 'Average' column is present, 
calculating the row-wise mean of available exam subjects after stripping whitespace from column names if needed. Next, it applies a compound boolean condition
to isolate records where 'Hometown' is 'Visayas' and 'Gender' is 'Female', selecting only the 'Name', 'Track', 'GEAS', 'Electronics', and 'Average' columns 
into the VisFemale DataFrame. After displaying the complete VisFemale table, it applies a secondary numerical filter (VisFemale['Average'] >= 60) to display 
only students who achieved an average of at least 60 without altering or overwriting the original VisFemale DataFrame. 


# PROBLEM C: CATEGORY-AVERAGE VISUALIZATION


## CODE

<img width="997" height="787" alt="image" src="https://github.com/user-attachments/assets/93b5005b-6ee5-43a1-a9a4-cfe566d680a8" />

<img width="995" height="563" alt="image" src="https://github.com/user-attachments/assets/a4cab9e8-d0d2-44fa-90dd-3956681b6e54" />

<img width="1002" height="382" alt="image" src="https://github.com/user-attachments/assets/03d95c6e-f4ff-41e8-9173-970e509f1044" />

## EXPLANATION
This code computes, visualizes, and interprets the mean exam performance across different student demographics. After cleaning column names and verifying 
the presence of the 'Average' score, it uses .groupby() to calculate and display the mean score for each category within 'Track', 'Gender', and 'Hometown'. 
It then plots these summaries side-by-side using a shared 0–100 vertical scale across three distinct bar charts, complete with labeled axes and titles.
Finally, it uses .idxmax() to dynamically locate the category with the highest sample mean for each demographic factor and prints concise, descriptive 
statements strictly detailing the observed dataset.
