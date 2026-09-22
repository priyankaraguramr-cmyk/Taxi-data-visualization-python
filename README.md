# Taxi-data-visualization-python
1. Project Overview
   
This project analyses NYC taxi trip data from the Seaborn “taxis” dataset, which holds 6,433 trips recorded in March 2019.The notebook
loads the data, handles the missing values, and builds ten visualizations with Pandas, Matplotlib and Seaborn to look at fare, distance,
payment method and pickup location.

2. Files in this Folder

File	Description
Taxi_Data_Visualization.ipynb	Main notebook with the code, all plots and a short observation under each plot Taxi_Analysis_Summary.docx	
One-page summary of the findings Readme document Python DA Assignment 2 -Data Visualization-Taxi_Data_Visualization.docx	This file

3. Requirements

•Python 3

•pandas, matplotlib and seaborn (seaborn 0.13 or later)

.An internet connection, because sns.load_dataset("taxis") downloads the data on first run Google Colab already includes 

all of these libraries.

5. How to Run the Notebook

Google Colab

1.Open Google Colab and choose File > Upload notebook.

2.Select Taxi_Data_Visualization.ipynb.

3.Choose Runtime > Run all.

5.Jupyter Notebook

1.Install the libraries: pip install pandas matplotlib seaborn notebook

2.Start Jupyter with the command jupyter notebook and open the file.

3.Choose Kernel > Restart & Run All.
The cells are meant to be run in order from top to bottom. No extra files need to be uploaded.

6. Notebook Structure

7.Section	Content

 1. Load the dataset	Imports the libraries and loads the taxis dataset
   
 2. Handle missing values	Finds the columns with missing data, then imputes or removes rows
   
 3. Matplotlib / Pandas plots	Line chart, bar chart, pie chart, histogram and box plot
   
 4. Seaborn plots	Count plot, scatter plot, heatmap, pair plot and violin plot
 
 5. Key findings summary	Small table of the main figures from the cleaned data
 
 6. Missing Value Handling
   
 7.Missing values were found only in categorical columns.

 Column	Missing	Treatment payment	44	Filled with the most frequent value dropoff_zone, dropoff_borough	45 each	Filled with the most frequent
 value pickup_zone, pickup_borough	26 each	Rows removed, since the pickup location is central to the analysis and cannot be reasonably guessed
 After cleaning, 6,407 of the 6,433 rows remain and no missing values are left.

8. Visualizations
 
 Plot	Library	What it shows Line chart	Matplotlib	Fare against pickup time, with a daily average line on top Bar chart	Pandas	Total fare for 
 each pickup borough Pie chart	Pandas	Share of trips by payment method Histogram	Matplotlib	Distribution of trip distance (60 bins) Box plot
 Pandas	Tip amount for each pickup borough Count plot	Seaborn	Number of trips in each pickup borough Scatter plot	Seaborn	Distance against fare,
 coloured by pickup borough Heatmap	Seaborn	Correlation of distance, fare, tip, tolls and total Pair plot	Seaborn	Distance, fare, tip and total,
 coloured by pickup zone Violin plot	Seaborn	Fare distribution for each payment method

9. Notes
    
 •The dataset has about 190 pickup zones, which would make the pair plot legend unreadable, so the pair plot uses the 5 busiest zones.

 •The daily average line in the line chart leaves out 28 February, which has only one trip.

 •Cash trips record a tip of zero, so tip comparisons between boroughs mostly reflect the mix of cash and card payments.

 •The Bronx has only 99 trips, so results for that borough should be read with care.
