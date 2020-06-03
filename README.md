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


# Workshop Agenda
-  Business Overview
  - Opportunities & Challenges to Forecast
  - Major Use Cases for Forecast

- Time Series Analysis Primer

- Algorithms Overview
  - Statistical Methods (ARIMA, NPTS, ETS)
  - ML Models (DeepAR+, Prophet)
  - A note on Pricing

- Customer Case Studies
  - Inventory/Capacity/Workforce Planning, 
  - Scenario Discussion
  - Summary & Identification of Next Steps

# Hands-on Lab Modules
  - Lab Module 1: Defining & Importing your data (Datasets, Exploration, Ingestion) 	
  - Lab Module 2.1: Creating and Evaluating Forecasts	TTS 		 				
  - Lab Module 2.2: Creating and Evaluating Forecasts	RTS

## Introduction to Amazon Forecast

If you are not familiar with Amazon Forecast you can learn more about this tool on these pages:

* [Product Page](https://aws.amazon.com/forecast/)
* [GitHub Sample Notebooks](https://github.com/aws-samples/amazon-forecast-samples)
* [Product Docs](https://docs.aws.amazon.com/forecast/latest/dg/what-is-forecast.html)


## Process:
1. Deploying Your Working Environment
1. Validating and Importing Target Time Series Data
1. Creating and Evaluating Your First Predictors
1. Importing Related Time Series Data
1. Creating and Evaluating Related Time Series Enabled Predictors
1. Next Steps



## Preparing for the Labs
#### Create an ML Notebook 

As described here: https://docs.aws.amazon.com/sagemaker/latest/dg/gs-setup-working-env.html While specifying notebook, select 

    - `Instance Type` as `t3.micro`
    - `Additional Configuration -> Volume Size in GB` and enter 5GB
    - Add following IAM policies to the IAM role attached to the SageMaker Notebook:
       - `AmazonSageMakerFullAccess`
       - `AmazonS3FullAccess` 
       
#### Download Lab Guides & SageMaker Sample Notebooks (in SageMaker)

    - Open SageMaker Terminal
    - Do `cd SageMaker`
    - Clone Lab Guides `git clone https://github.com/CloudaYolla/ForecastPOC.git`
    - Clone SageMaker examples `git clone https://github.com/aws-samples/amazon-forecast-samples.git`


### Cleaning up resources 

The scripts in this POC provision various Forecast, S3, and IAM resources. If you ran this POC in your own account and would like to avoid ongoing charges related to these resources, open `Cleanup.ipynb` and run the cleanup scripts provided there. Wait for the scripts to complete, then tear down the CloudFormation stack you created at the beginning of these instructions.


**Very Important:** SageMaker Notebooks run on EC2, and therefore you will be billed by the second unless you save your work (by downloading to your local computer) & terminate the SageMaker notebook instance. 

Please 
 1. download the notebook (if you did any changes) to your computer by selecting ` File -> Download as -> Notebook (.ipynb)`. 
 1. Terminate this instance. Remember that you can always recreate it from the `AWS SageMaker Console` again.  
 
## Next Steps

Identify your use case and data sources, and start testing Amazon Forecast. Contact your AWS team for PoC/pilot support.

Thank you.

