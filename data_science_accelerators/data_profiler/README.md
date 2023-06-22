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

7. Add your login info and dataset ID, and click Login
8. Select the features you wish to run, and a page name for the output, and click Run Scaffolding

### Step 2: Fill Out the Login Widget

Fill out the login widget with your instance name, email, password, and the dataset ID you are running the profiler on. If your instance doesn't support Direct Sign-On, select the SSO option, and enter your session cookie instead of your email and password. You can find the session cookie with the following steps:
1. Login into the instance in a separate window
2. Open the browser's developer tools (you can usually do this by right-clicking anywhere on the page and clicking *inspect*)
3. Select the *Application* tab
4. Expand the *Cookies* menu on the left side, and select the instance URL
5. Find the cookie named "DA-SID-***" (or something similar), and copy the value

After entering your Direct/SSO login information, click *Login*, and you should see “Login Successful” near the bottom of the widget.


## Questions?
Contact datascienceSME@domo.com
