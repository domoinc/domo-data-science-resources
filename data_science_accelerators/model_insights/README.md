<img src="https://github.com/domoinc/domo-data-science-resources/blob/02297d262c1a5b6113e88554483f0d872b2086ba/data_science_accelerators/images/Domo_logo.png" alt="Image Description" width="200">

# Model Insights Accelerator

## Requirements
The Model Insights Accelerator currently supports the use of Regression and Binary Classification Models. The tool requires a pickled (saved) model, training dataset (data upon which the pickled model was built), and a live dataset (data for which predictions will or have been made).

## Overview 
The Model Insights Accelerator creates a comprehensive dashboard that displays the following model insights: 
- **Overview page**: displays model name, model type, model class, model train date, insights last update, & model pipeline function
<img src="https://github.com/domoinc/domo-data-science-resources/blob/b7b1cf8e12a1fef47ff28cdb316d300c48b1e629/data_science_accelerators/images/Model%20Insights%20Overview.jpg" alt="Image Description" width="1000">

- **Monitoring page**: displays current and historical prediction accuracy metrics (accuracy, F1, precision, recall, specificity, confusion matrix) & data drift (both overall and feature drift)
<img src="https://github.com/domoinc/domo-data-science-resources/blob/b7b1cf8e12a1fef47ff28cdb316d300c48b1e629/data_science_accelerators/images/Model%20Insights%20Monitoring.jpg" alt="Image Description">

- **Prediction Explainer page**: displays feature contributions (SHAP values) by row/observation & Partial Dependence Plots (PDP) by observation
<img src="https://github.com/domoinc/domo-data-science-resources/blob/4e7f7148a42c0713e1dce5c87ba70d524d971c57/data_science_accelerators/images/Model%20Insights%20Prediction%20Explainer.jpg" alt="Image Description" width="1000">

- **Training Performance page**: displays accuracy metrics (accuracy, F1, precision, recall, specificity, confusion matrix) by threshold, ROC Curve, & Precision-Recall Curve. **Note: all of these metrics are based on your training data.** 
<img src="https://github.com/domoinc/domo-data-science-resources/blob/4e7f7148a42c0713e1dce5c87ba70d524d971c57/data_science_accelerators/images/Model%20Insights%20Training%20Performance.jpg" alt="Image Description">

- **Feature Importance page**: displays overall feature importance, feature dependence, correlations between features, & Variance Inflation Factors (VIF)
<img src="https://github.com/domoinc/domo-data-science-resources/blob/4e7f7148a42c0713e1dce5c87ba70d524d971c57/data_science_accelerators/images/Model%20Insights%20Feature%20Importance.jpg" alt="Image Description" width="1000">



## Walkthrough Video
Watch this [walkthrough video](https://drive.google.com/file/d/1C7ssyocGBzC-ahXOCMODI8acta28yPHY/view) which shows how to prepare for and use the Model Insights Accelerator.

## Instructions
1. Download ```.tar``` file [here](https://github.com/domoinc/domo-data-science-resources/blob/main/data_science_accelerators/model_insights/model_insights.tar) (click “View raw” or “Download”).
2. In your Domo instance, create a Jupyter workspace that uses a **Python** kernel. See [here](https://domo-support.domo.com/s/article/36004740075?language=en_US#creating_workspace) for additional help.
3. Start/run the Jupyter workspace created in step 2. See [here](https://domo-support.domo.com/s/article/36004740075?language=en_US#running_workspace) for additional help.
4. In your running Jupyter workspace, upload the ```.tar``` file downloaded in step 1 by selecting the **Upload Files** button located in the left panel of the workspace. 
5. Also in your running Jupyter workspace, open a new terminal window by selecting **File > New > Terminal**. Type the following code in the terminal window and hit **Enter**: ```tar xf model_insights.tar```. This will enable use of examples and all source files for the model insights tool.
6. Also type the following code in the terminal window and hit **Enter** in succession: ```cd model_insights``` and then ```pip install -r requirements.txt```. This code installs package versions required for proper functioning of the tool.
7. Follow instructions in [walkthrough video](https://drive.google.com/file/d/1C7ssyocGBzC-ahXOCMODI8acta28yPHY/view).


## Questions?
Contact datascienceSME@domo.com
