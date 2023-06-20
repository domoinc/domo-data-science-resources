<!--
    Right-Click > Open With > Markdown Preview
-->

# Data Profiler Usage Guide

## Step 1 – Login

Fill out the login form with your instance name, email, password, and the dataset ID you are running the profiler on. If your instance doesn't support Direct Sign-On, select the SSO option, and enter your session cookie instead of your email and password. You can find the session cookie with the following steps:
1. Login into the instance in a separate window
1. Open the browser's developer tools (you can usually do this by right-clicking anywhere on the page and clicking *inspect*)
1. Select the *Application* tab
1. Expand the *Cookies* menu on the left side, and select the instance URL
1. Find the cookie named "DA-SID-***" (or something similar), and copy the value

After entering your Direct/SSO login information, click *Login*, and you should see “Login Successful” near the bottom of the form.

![step1](./imgs/step1.png)

**NOTES:**
* The instance field should be the instance name (without the “.domo.com”)
* The password field is cleared and deleted from memory after logging in, so you’ll need to re-enter your password (and re-login) if you run the profiler again with a different dataset

## Step 2 – General

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

![step3](./imgs/step3.png)

## Step 4 – Bias

**NOTE:** This feature is only available for categorical inferences (as determined by the selections in the previous step). The Bias Profile calculates metrics similar to those used with AWS SageMaker Clarify, a tool for detecting and explaining data bias. After selecting the “positive” label from the dataset’s target column, this feature creates a dataflow that calculates the bias metrics, and a few cards to visualize the results. A separate card is also created that explain the various metrics.

![step4](./imgs/step4.png)

## Step 5 – Other

**Optional:** Select a column to create line charts against (primarily intended for time series plots, but you can technically use any numeric feature).

![step5](./imgs/step5.png)

## Step 6 – Run the Profiler

When all your selections are made, you can click Run Profile. Similar to the Login process, you will see the output of the profiler below the form. When you see the message “finished scaffolding”, the profiler has finished, and you can go check the dashboard view in Domo to see the results.