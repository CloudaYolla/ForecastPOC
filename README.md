![ML Logo](images/logo.png "Logo") 

# Amazon Forecast - A Hands-on Workshop tailored for Data Scientists


# Amazon Forecast
Companies today use everything from simple spreadsheets to complex planning software to attempt to accurately forecast future business outcomes such as

-	Retail product demand, such as the demand for products selling on a website or at a particular store or location
-	Supply chain demand including the quantity of raw goods, services, or other inputs needed by manufacturing
-	Resource requirements, such as the number of call center agents, contract workers, IT staff, and energy needed to meet demand
-	Operational metrics, such as web traffic to servers, AWS usage, or IoT sensor usage
These tools build forecasts by looking at a historical time series of data. This approach can struggle to produce accurate forecasts for large sets of data that have irregular trends multiple data series that change over time.

Based on the same technology used at Amazon.com, Amazon Forecast uses machine learning to combine time series data with additional variables to build forecasting models capable of making predictions that are up to 50% more accurate than looking at time series data alone.

# Objectives
By the end of this POC progress you should have picked up the following skills:

-	How to map input dataset to Amazon Forecast.
-	Comparison of algorithms such as DeepAR+ Prophet, ETS
-	To interpret model metrics.
-	To deploy models in a programmatic fashion.
-	To obtain results from Forecast

# Audience
-	Data Scientists, Data Engineers who have experience in EDA & Model Development in Python using Jupyter Notebooks.

# Prerequisites:

-	The workshop below is a (Level 300) deep dive designed to help you build out your first models for your given use case.
-	Bring your own AWS account: The workshop will be based on sample scenarios and will be run at each participant’s own AWS account. Please make you have sufficient permissions for the services (Forecast, SageMaker, S3, IAM)


# Workshop Audience
-  Business Overview
  - Opportunities & Challenges to Forecast
  - Major Use Cases for Forecast

  - Amazon Forecast Unique benefits: Related datasets, Cold Starts

- Algorithms Overview
  - Statistical Methods (ARIMA, NPTS, ETS)
  - ML Models (DeepAR, Prophet)
  - Major Challenges of Recommendation Systems
  - High Variation, Regional demand, New items (cold start), High Seasonality
  - Enriching Dataset with Related Time Series Data
  - A note on Pricing

- Customer Case Studies
  - Inventory/Capacity/Workforce Planning, 
  - Scenario Discussion
  - Summary & Identification of Next Steps

# Hands-on Lab Modules
  - Lab Module 1: Defining your data (Datasets, Schemas, Exploration, Ingestion) 	
  - Lab Module 2.1: Creating a Predictor 		 				
  - Lab Module 2.2: Evaluating Solutions	
  - Lab Module 3: Deploying Model & Predicting				 


## Introduction to Amazon Forecast

If you are not familiar with Amazon Forecast you can learn more about this tool on these pages:

* [Product Page](https://aws.amazon.com/forecast/)
* [GitHub Sample Notebooks](https://github.com/aws-samples/amazon-forecast-samples)
* [Product Docs](https://docs.aws.amazon.com/forecast/latest/dg/what-is-forecast.html)


## Process:

1. Deploying Your Working Environment
1. Validating and Importing Target Time Series Data
1. Validating and Importing Related Time Series Data (To Test)
1. Creating and Evaluating Your First Predictors
1. Importing Related Time Series Data (To Use)
1. Creating and Evaluating Related Time Series Enabled Predictors
1. Next Steps






## Validating and Importing Target Time Series Data

Open `Validating_and_Importing_Target_Time_Series_Data.ipynb` and follow along there.

Once this has completed you can move onto prepping your Related Time Series data though you may not want to actually delete it after the import completes. 
If the data resides within your DatasetGroup then models will use it automatically when you train them and you are not able to determine the impact of just your base time series data easily.

## Validating and Importing Related Time Series Data

Amazon Forecast can certainly generate predictions using only the target data but the real power of the service comes into play when adding related time series information to facilitate better understanding of external signals, as well as item metadata that allows DeepAR+ to make assumptions about how a time series may behave when missing chunks of information.

Open `Validating_and_Importing_Related_Time_Series_Data.ipynb` and follow along there to prepare the dataset for the POC/Amazon Forecast.

## Creating and Evaluating Your First Predictors

In Amazon Forecast a model that has been trained on your data is called a Predictor, the notebook below will guide you through using the data you imported earlier to build your first predictors. At the end there is a bonus bit on running AutoML to determine the best. This is advised to be done before going home for the day as the process will take a number of hours to complete.

Open `Creating_and_Evaluating_Predictors.ipynb` and follow along to build these Predictors and see their results.

## Importing Related Time Series Data

Upon completing the initial models with just the target time series data go back to `Validating_and_Importing_Related_Time_Series_Data.ipynb` and execute the import job again if you deleted it during your validation phase. Once the data has been imported you are ready to move onto the next session of building a model with the related data.

## Creating and Evaluating Related Time Series Enabled Predictors

During this section you'll only be creating new models with Prophet and DeepAR+ this is because they are the only algorithms to incorporate related time series into their forecasts at this time within the service. As existing algorithms are modified or new ones are introduced this section will expand to cover those.

To get started simply open `Creating_and_Evaluating_Related_Time_Predictors.ipynb` this will be the last section of the POC that is guided and the rest will be an exploratory analysis to determine the value of any improvements.

## Next Steps

Identify your use case and data sources, and start testing Amazon Forecast. Contact your AWS team for PoC/pilot support.

## Cleanup

The scripts in this POC provision various Forecast, S3, and IAM resources. If you ran this POC in your own account and would like to avoid ongoing charges related to these resources, open `Cleanup.ipynb` and run the cleanup scripts provided there. Wait for the scripts to complete, then tear down the CloudFormation stack you created at the beginning of these instructions. 
