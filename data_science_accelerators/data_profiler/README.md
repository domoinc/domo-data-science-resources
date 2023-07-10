<img src="https://github.com/domoinc/domo-data-science-resources/blob/02297d262c1a5b6113e88554483f0d872b2086ba/data_science_accelerators/images/Domo_logo.png" alt="Image Description" width="200">


# Data Profiler Accelerator

## Overview 
The Data Profiler Accelerator conducts an automated exploratory analysis of all variables in your dataset and then creates a Domo dashboard, which can include the following types of cards: 
- Correlation matrix card that shows the correlations between variables
- Histogram and bar chart cards that show the distribution of variables
- Scatterplot and bar chart cards that show the relationships between variables

<img width="900" alt="image" src="https://github.com/domoinc/domo-data-science-resources/blob/d97f9a06e3fc22a9f9b08aedd4c2f5438dec7386/data_science_accelerators/images/data_profiler_correlations.png">

<img alt="image" src="https://github.com/domoinc/domo-data-science-resources/blob/d97f9a06e3fc22a9f9b08aedd4c2f5438dec7386/data_science_accelerators/images/data_profiler_histograms_barchart.png">




## Video Demo
[Video Demo of Data Profiler](https://www.youtube.com/watch?v=9CXoYW-wG-g&t=2588s)


## Instructions

### Step 1: Set-Up
1a. Download the ```DataProfilerGUI_v5.ipynb``` notebook file by going [here](https://github.com/domoinc/domo-data-science-resources/blob/main/data_science_accelerators/data_profiler/DataProfilerGUI_v5.ipynb)

1b. In your Domo instance, create a Jupyter workspace that uses a **Python** kernel. See [here](https://domo-support.domo.com/s/article/36004740075?language=en_US#creating_workspace) for additional help.

1c. Start/run the Jupyter workspace created in step 2. See [here](https://domo-support.domo.com/s/article/36004740075?language=en_US#running_workspace) for additional help.

1d. In your running Jupyter workspace, upload the ```.ipynb``` notebook file downloaded in step 1 by selecting the **Upload Files** button located in the left panel of the workspace. Open the ```.ipynb``` notebook file by selecting the file, which should be listed in the file browser in the left panel of the workspace.

1e. Run the cells in this notebook file by selecting **Run > Run All Cells**. If the cells ran correctly, when you scroll down to nearly the bottom of the notebook file, you should see a Login widget (pictured below).
  <img width="568" alt="image" src="https://github.com/domoinc/domo-data-science-resources/assets/123829195/07384295-b21b-49ff-bf1d-7c3e852f4eab">


### Step 2: Fill in the Login Widget

2a. Fill in the login widget with your Domo instance name (without the “.domo.com”), your email associated with your Domo instance, your password associated with your Domo instance, and the dataset ID you are running the profiler on. If your instance doesn't support Direct Sign-On, select the SSO option, and enter your session cookie instead of your email and password. You can find the session cookie with the following steps:
  1. Login into the instance in a separate window
  2. Open the browser's developer tools (you can usually do this by right-clicking anywhere on the page and clicking *inspect*)
  3. Select the *Application* tab
  4. Expand the *Cookies* menu on the left side, and select the instance URL
  5. Find the cookie named "DA-SID-***" (or something similar), and copy the value

2b. After entering your Direct/SSO login information, click *Login*. If successful, the phrase “Login Successful” should appear below the Login widget.

<img width="614" alt="image" src="https://github.com/domoinc/domo-data-science-resources/assets/123829195/e6d382cc-3d10-4a37-8e6d-0a34a068c889">


Note: The password field is cleared and deleted from memory after logging in, so you’ll need to re-enter your password (and re-login) if you run the profiler again with a different dataset


### Step 3: Fill in Remaining Widgets

Below the Login widget in your notebook file, you should see four other widgets named General, Inference, Bias Profile, and Other. Follow the instructions below to fill in these widgets (note: some steps are required while others are optional). 

**3a. General Widget**
* *Page Name:* Specify the dashboard name for the profiler output 
* *Tags:* List tag names for the resources created during the profiler (optional)
* *Correlation Profile:* Creates a dataflow that creates a correlation matrix between the numeric features of the dataset, and creates a card to display this matrix (optional)
* *Histogram Profile:* Creates a histogram for each feature in the dataset (optional)

<img width="480" alt="image" src="https://github.com/domoinc/domo-data-science-resources/assets/123829195/579a0cab-320c-4815-baa2-856ee6751ef1">

**3b. Inference Widget** (note: filling in this widget is optional) 
* *Dependent Variable:* Select the dependent variable, which will be the target of the subsequent inference
* *Inference Type:* Select the inference type
* *Feature Engineering Flow:* Creates a simple dataflow that maps the source dataset to a new set, which is then used in all subsequent card building / dataflows. While this selection doesn’t actually do any feature engineering, it creates a flow at the top of the pipeline which you can edit
* *Validation Flow:* Sets up a validation dataflow and accompanying webform that can be used to validate incoming data (based on the criterea of the webform)
* *Model Flow:* Sets up a dataflow with a simple model using the Scripting Tiles. Similar to the Feature Engineering Flow, this is more of a template for you to edit afterwards
* *Scatterplot Profile:* This feature creates scatterplots for the dependent variable vs all variables in your dataset
* *Boxplot Profile:* This feature creates boxplots for the dependent variable vs all other variables in your dataset

<img width="499" alt="image" src="https://github.com/domoinc/domo-data-science-resources/assets/123829195/1bd43edc-f136-47ce-be23-cced9a5d9a50">


**3c. Bias Profile Widget** (note: filling in this widget is optional) 

The Bias Profile calculates metrics similar to those used with AWS SageMaker Clarify, a tool for detecting and explaining data bias. This widget creates a dataflow that calculates the bias metrics and a few cards to visualize the results. A separate card is also created that explain the various metrics. **This widget is only available for categorical inferences.**

* In order for the Bias Profile Widget to work, you need to fill in the *Dependent Variable* and *Inference Type* fields in the Inference Widget (see Section 3b. Inference Widget above). *Inference Type* should be set to "Categorical"
* *Positive Label:* Indicate the “positive” label of your dependent variable  

<img width="493" alt="image" src="https://github.com/domoinc/domo-data-science-resources/assets/123829195/e693efa2-61b9-4dc7-bacb-72549979ba14">


**3d. Other Widget** (note: filling in this widget is optional)

This widget creates line charts for a selected variable vs other variables in your dataset 

* *Time Series Plot X-Axis:* Select a variable that will be plotted on the x-axis of all the line charts (frequently this is a datetime variable, but you can technically specify any numeric variable)

<img width="497" alt="image" src="https://github.com/domoinc/domo-data-science-resources/assets/123829195/d486813a-1e98-43b5-b5f4-594d6653e1e0">



### Step 4: Run the Profiler

4a. After you have filled in the widgets described in Step 3, click *Run Profile* at the bottom of the notebook file. Similar to the login process, you will see some output appear in the notebook file. When you see the message “finished scaffolding”, the profiler has finished running. A dashboard that displays all of the profiler output should now be availabe in your Domo instance.



## Questions?
Contact datascienceSME@domo.com
