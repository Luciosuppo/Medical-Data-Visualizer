# Medical Data Visualizer
This is the boilerplate for the Medical Data Visualizer project. It´s the third project of 5 to obtain the Data analyst with python certification from the FreeCodeCamp page.

## Instructions
In this project, you will visualize and make calculations from medical examination data using matplotlib, seaborn, and pandas. The dataset values were collected during medical examinations.

The rows in the dataset represent patients and the columns represent information like body measurements, results from various blood tests, and lifestyle choices. You will use the dataset to explore the relationship between cardiac disease, body measurements, blood markers, and lifestyle choices.

## Tasks
Create a chart similar to examples/Figure_1.png, where we show the counts of good and bad outcomes for the *cholesterol*, *gluc*, *alco*, *active*, and *smoke* variables for patients with cardio=1 and cardio=0 in different panels.

Use the data to complete the following tasks in medical_data_visualizer.py:

*   Add an overweight column to the data. To determine if a person is overweight, first calculate their BMI by dividing their weight in kilograms by the square of their height in meters. If that value is > 25 then the person is overweight. Use the value 0 for NOT overweight and the value 1 for overweight.
*   Normalize the data by making 0 always good and 1 always bad. If the value of cholesterol or gluc is 1, make the value 0. If the value is more than 1, make the value 1.
*   Convert the data into long format and create a chart that shows the value counts of the categorical features using seaborn's catplot(). The dataset should be split by 'Cardio' so there is one chart for each cardio value. The chart should look like examples/Figure_1.png.
*   Clean the data. Filter out the following patient segments that represent incorrect data:
    *   diastolic pressure is higher than systolic (Keep the correct data with (df['ap_lo'] <= df['ap_hi']))
    *   height is less than the 2.5th percentile (Keep the correct data with (df['height'] >= df['height'].quantile(0.025)))
    *   height is more than the 97.5th percentile
    *   weight is less than the 2.5th percentile
    *   weight is more than the 97.5th percentile
*   Create a correlation matrix using the dataset. Plot the correlation matrix using seaborn's heatmap(). Mask the upper triangle. The chart should look like examples/Figure_2.png.

## Files

* *medical_data_visualizer.py*: is where the code is written.
* *test_module.py*: contains the tests that is necessary for the correction.
* *main.py*: file that must be run to test the code.
* *medical_data_visualizer.ipynb*: is a notebook file that contains the questions and the code to answer them.
* *medical_examination.csv*: is the csv file where the data is stored.