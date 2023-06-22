<img width="212" alt="image" src="https://github.com/domoinc/domo-data-science-resources/assets/123829195/64b7e595-a5ef-41bb-bac6-81f482f5d177">


# Data Profiler Accelerator

## Overview 
The Data Profiler Accelerator conducts an automated exploratory analysis of all variables in your dataset and then creates a Domo dashboard with the following cards: 
- correlation matrix card that shows the correlations between variables;
- histogram and bar chart cards that show the distribution of variables; and
- scatterplot and bar chart cards that show the relationships between variables


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


### Step 2: Fill In the Login Widget

2a. Fill in the login widget with your Domo instance name (without the “.domo.com”), your email associated with your Domo instance, your password associated with your Domo instance, and the dataset ID you are running the profiler on. If your instance doesn't support Direct Sign-On, select the SSO option, and enter your session cookie instead of your email and password. You can find the session cookie with the following steps:
  1. Login into the instance in a separate window
  2. Open the browser's developer tools (you can usually do this by right-clicking anywhere on the page and clicking *inspect*)
  3. Select the *Application* tab
  4. Expand the *Cookies* menu on the left side, and select the instance URL
  5. Find the cookie named "DA-SID-***" (or something similar), and copy the value

2b. After entering your Direct/SSO login information, click *Login*. If successful, the phrase “Login Successful” should appear below the Login widget.

<img width="614" alt="image" src="https://github.com/domoinc/domo-data-science-resources/assets/123829195/e6d382cc-3d10-4a37-8e6d-0a34a068c889">


**NOTES:**
* The password field is cleared and deleted from memory after logging in, so you’ll need to re-enter your password (and re-login) if you run the profiler again with a different dataset


### Step 3: Fill in Other Widgets

Below the Login widget in your notebook file, you should see four other widgets named General, Inference, Bias Profile, and Other. Follow the instructions below to fill in these widgets (note: some steps are required while others are optional). 

#### General Widget
  **Required:** Specify the page name for the profiler output

  **Optional:** List tag names for the resources created during the profiler, and select the correlation and histogram profile features
  * *Correlation Profile* – creates a dataflow that creates a correlation matrix between the numeric features of the dataset, and creates a card to display this matrix
  * *Histogram Profile* – creates a histogram for each feature in the dataset

![step2](./imgs/step2.png)

## Step 3 – Inference

**Optional:** Select the dependent variable / target of the inference, you can also select the inference type. Once selected, you can select the following features:
* *Feature Engineering Flow* – creates a simple dataflow that maps the source dataset to a new set, which is then used in all subsequent card building / dataflows. While this selection doesn’t actually do any feature engineering, it creates a flow at the top of the pipeline which you can edit
* *Validation Flow* – Sets up a validation dataflow and accompanying webform that can be used to validate incoming data (based on the criterea of the webform)
* *Model Flow* – Sets up a dataflow with a simple model using the Scripting Tiles. Similar to the Feature Engineering Flow, this is more of a template for you to edit afterwards
* *Scatterplot Profile* – This feature creates scatterplots for the dependent variable vs all other columns in the dataset
* *Boxplot Profile* – This feature creates boxplots for the dependent variable vs all other columns in the dataset

## Questions?
Contact datascienceSME@domo.com
