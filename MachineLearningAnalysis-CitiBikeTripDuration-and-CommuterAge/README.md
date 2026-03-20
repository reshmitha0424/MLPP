# <u>MachineLearningAnalysis - CitiBike TripDuration and CommuterAge</u>
![alt text](https://d21xlh2maitm24.cloudfront.net/nyc/01unlock2.JPG?mtime=20160428123800)
### ***Overview:***

Bike share programs have been implemented in cities around the world in an effort to address multiple aspects of both city functioning and quality of life for urban populations. Traffic congestion, public health, community engagement, and air quality have all aspects of city life that could potentially be impacted by the introduction of a bike share program into a community.

One particularly massive bike share is New York City's Citi Bike program. The area coverage of this program is large (extending into New Jersey across the Hudson River) and ridership initial adoption rates – as measured by the number of rides taken – were promising. However this program has not been without controversy and there has been active discussion regarding which communities ara actually being served and which are not, who is benefitting from the availability of bikes, how they are being used for recreational vs commuter purposes, etc.

The goal of this project is two-fold: 
<ul>
  <li>learn to work with basic tabular data from the Citi Bike program </li>
  <li>generate a simple estimate for the which age group is predominantly using citi bikes for commuter travel.</li>
</ul>

<hr>

### ***Background:***

Good data science (and data analysis more generally) as well as the appropriate application of machine learning algorithms depends on a clear understanding of the underlying problem/situation, the methods by which the data you are about to analyze are collected, and the situational context in which that data sits.  To that end:

<b>

Read through the following resources (including links within) regarding the Citi Bike program and its impacts in NYC,

1. [Official Citi Bike site](https://citibikenyc.com/)

2. [DOT Facts on Citi Bike](https://www.nyc.gov/html/dot/html/pr2013/facts-on-citi-bike.shtml)

3. [Cycling in the City](https://www.nyc.gov/html/dot/downloads/pdf/cycling-in-the-city-2020.pdf)

4. [The Rise of Citi Bikes in New York City](https://thesciencesurvey.com/news/2021/03/21/the-rise-of-citi-bikes-in-new-york-city/)

</b>

<hr>

### ***Dataset:***

**Source** - CitiBike trip data (April 2016)

**Google Link to the Source** - https://citibikenyc.com/system-data 

When you scroll down, you'll find a link named as "Download Citi Bike trip history data". Click on it to access different years' data for Citiike trips. 

<hr>

### ***Objectives:***
<ol>
  <li>Understand the distribution of trip durations.</li>
  <li>Identify whether the trip duration follows a normal (Gaussian) distribution.</li>
  <li>Classify trips as short (likely commuter trips) and long (likely recreational trips).</li>
  <li>Determine which age group takes the highest fraction of short trips.</li>
</ol>

### ***Methodology:***
<ol>
<li>Preprocessing: Load and clean the dataset.</li>
<li>Feature Engineering:</li>

<ul>
<li>Compute rider age from Birth Year.</li>
<li>Take the log of Trip Duration for better distribution analysis.</li>
  
</ul>
<li>Exploratory Data Analysis (EDA):</li>
<ul>
  <li>Visualize trip duration and log-transformed duration.</li>
  <li>Determine the median of log-transformed durations to categorize trips.</li>
</ul>

<li>Classification of Trips:</li>
<ul>
  <li>Define short_trip (below median) and long_trip (above median).</li>
  <li>Group data by age and analyze short-trip prevalence.</li>
</ul>


<li>Insights & Conclusions:</li>
<ul>
  <li>Identify which age groups commute the most.</li>
  <li>Evaluate if trip duration correlates with commuter behavior.</li>
</ul>
</ol>

### ***Key Findings:***
<ul>
  <li>The distribution of raw trip duration is positively skewed and not Gaussian.</li>
  <li>The log-transformed trip duration is closer to a normal distribution.</li>
  <li>The median trip duration (~6.85 min) is a reasonable estimate for short commuter trips.</li>
  <li>The age group with the highest proportion of short trips is identified.</li>
</ul>

<hr>

### ***Instructions on Running the code:***

There are two options for including the dataset in your Google Colab notebook. The procedure that is included in the code uses the method of mounting Google Drive. Here's a breakdown of both options:

**Option 1:**
<ul>
  <li>
    Using Google Drive (Mounting Google Drive) - Recommended in the Code
    In the provided code, we are using Google Drive to store and access the dataset. 
    The code already includes the necessary procedure to mount Google Drive. Just run the code in a Colab cell and follow the necessary steps
  </li>
  <li>
    After mounting Google Drive, update the fname variable with the correct path to your dataset stored in Google Drive. 
  </li>
  <li>Run the notebook cells sequentially.</li>
</ul>

**Option 2:**
<ul>
  <li>
    On the left panel of your Google Colab notebook, you’ll find an option to upload files.
    <ul>
      <li>Click on the Files tab (the folder icon).</li>
      <li>You'll see an Upload button. Click on it and select the dataset file from your local machine.</li>
    </ul>
  </li>
  <li>
    After uploading the file, it will appear in the Files section on the left. Right-click on the file and copy the file path. Update the fname variable with the copied file path 
  </li>
  <li>Run the notebook cells sequentially.</li>
</ul>














