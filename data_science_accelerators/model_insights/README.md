<img src="https://github.com/domoinc/domo-data-science-resources/blob/02297d262c1a5b6113e88554483f0d872b2086ba/data_science_accelerators/images/Domo_logo.png" alt="Image Description" width="200">

# Model Insights Accelerator

## Overview 
The Model Insights Accelerator creates a comprehensive dashboard that displays the following model insights: 
- Live model performance evaluation
- Model monitoring (monitors overall and feature drift as well as proper model pipeline function)
- Feature importance and correlations
- Insights into individual predictions
- Training performance evaluation

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
