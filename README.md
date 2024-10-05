# Data-Science-Internship

## Data Science Internship At Technocolabs Software

## Project 1: AttritionForecast-Analysis-and-Prediction

### Project Overview

AttritionForecast: Analysis and Prediction repository! This project focuses on analyzing employee attrition and building predictive models to forecast future attrition rates. By understanding the factors influencing employee turnover, we aim to provide actionable insights to improve employee retention strategies.  
Employee attrition is a significant concern for many organizations as it impacts productivity, morale, and costs. This project aims to analyze historical employee data to identify key factors influencing attrition and to build predictive models that can help forecast future attrition rates.  

### Task Sumrray
This project aims to provide insights into the factors influencing employee attrition and predict which employees are likely to leave the company. 
Let's refine the project to make it more closely aligned with real-time scenarios and address live problem statements within an organization.  

#### Business Intelligence (BI) Analysis:

1. Data Exploration and Visualization:
- Create interactive dashboards using BI tools to visualize trends and patterns in employee turnover.
- Identify departments, roles, and specific projects with the highest turnover rates.
  
2. Descriptive Analytics:
- Generate reports that highlight the primary reasons for attrition based on employee feedback, exit interviews, and other relevant sources.
- Analyze the impact of factors like job satisfaction, workload, and career growth on employee turnover.
  
3. Predictive Analytics with BI:
- Build predictive models within the BI tools to estimate the likelihood of turnover for current employees.
- Implement scenario analysis to understand the potential impact of changes in satisfaction levels, compensation, or management practices.

#### Machine Learning Model:

1. Data Preprocessing:
- Incorporate real-time data feeds from HR systems to ensure the model is continuously updated.
- Dynamically handle new employee entries and update the model as employees leave or join.

2. Feature Engineering:
- Include features such as recent performance reviews, project completion milestones, and employee engagement scores for a more accurate prediction.

3. Model Training and Monitoring:
- Implement a mechanism to retrain the machine learning model periodically with the latest data.
- Set up monitoring to alert HR teams when an employee's predicted turnover likelihood surpasses a certain threshold.

4. Integration with BI Tools:
- Embed live predictions from the machine learning model into the BI dashboards.
- Enable HR managers to drill down into specific departments or teams to identify high-risk individuals and take proactive measures.

#### Real-time Scenarios and Impact:

1. Proactive Employee Retention:
- HR managers can use the integrated BI tools to identify high-risk employees and take proactive measures to address their concerns.
- Real-time alerts enable timely interventions, such as personalized career development plans or targeted retention efforts.

2. Strategic Workforce Planning:
- HR leaders can leverage predictive analytics to inform strategic workforce planning, ensuring that teams critical to ongoing projects are adequately supported.

3. Continuous Improvement:
- Regular updates to the machine learning model based on real-time data allow for continuous improvement in prediction accuracy.
- Feedback loops from HR teams can be integrated into the model to enhance its effectiveness over time.
  
### conclusion : 
By addressing the live problem statement of employee turnover at Acme Corporation, this project integrates BI tools and machine learning to provide actionable insights and empower the organization to proactively manage its workforce. The real-time nature of the analysis ensures that decision-makers have up-to-date information for effective interventions.

## Project 2: MSB Project

### Project Overview
This project aims to build a machine learning pipeline integrating two models: a Gradient Boosting Machine (GBM) for binary classification and a Lasso regression model for continuous prediction.   
The objective is to evaluate delinquency and prepayment risks in mortgage loans using a Flask-based web application. 
The system generates predictions for both loan default risks and prepayment rates based on user input.

### Task Summary

#### Task 1: Data Preprocessing
- Data Cleaning: Remove inconsistencies and errors from the dataset to ensure accuracy.  
- Data Encoding: Convert categorical data into numerical formats for analysis.  
- Data Labelling: Assign labels to classify different elements in the dataset.
   
#### Task 2: Case Study on Mortgage Loans  
- Conduct a detailed analysis of mortgage loan data to identify trends, risks, and opportunities.  
- Summarize findings in a report.
  
#### Task 3: Exploratory Data Analysis (EDA)
- Univariate Analysis: Analyze the distribution of individual features.
- Bivariate Analysis: Examine relationships between pairs of features.
- Multivariate Analysis: Analyze interactions between multiple features using advanced techniques like PCA and correlation matrices.
  
#### Task 4: Feature Engineering
- Feature Selection: Identify and retain important features.
- Creation of New Features: Generate new features based on domain knowledge or data insights.
- Normalization and Scaling: Standardize features to prevent dominance during model training.
- Encoding Categorical Variables: Convert categorical variables using methods like one-hot encoding.
  
#### Task 5: Prepayment Variable Creation
- Based on available data, derive a prepayment variable to be used in regression models.
  
#### Task 6: Model Integration and Pipeline
- Binary Classification: Use GBM to classify loan default risks.
- Regression Model: Use Lasso regression to predict prepayment rates.
- Pipeline Creation: Create a pipeline that integrates both models for streamlined prediction.
- Testing and Evaluation: Ensure proper functioning and evaluate using suitable metrics.
- Documentation: Thoroughly document the pipeline with detailed comments and explanations.

#### Final Task: 
This task aims to build a machine learning pipeline integrating a Gradient Boosting Machine (GBM) for binary classification and a Lasso regression model for continuous prediction to evaluate delinquency and prepayment risk in mortgage loans. 
Implemented as a Flask-based web application, it allows users to input key mortgage-related data, generating two predictions: a classification to assess the likelihood of loan default and a regression to estimate the prepayment rate, offering a comprehensive analysis of loan risk.

### Project Structure

```bash
Mortgage-Prediction/
│
├──model/
│    └── MortgagePipelineModel.pkl                     
├── requirements.txt  
├── .env
├── logs/
├── static/
│   └── images/
│   └── css/ 
│       └── index.css    
│       └── result.css     
│
├── templates/
│   └── index.html         
│   └── results.html      
│               
├── Pipeline_Handler.py              
├── app.py           
└── README.md    

```


###  Pipeline Overview :
The pipeline is structured as follows:
- Data preprocessing is done before feeding it into the models.
- The GBM model classifies the data, filtering relevant instances.
- The filtered data is passed to the Lasso regression model to predict the prepayment rate.

###  Model Integration :
The models are integrated into a single workflow:
- The GBM model filters the dataset to identify delinquent loans.
- The Lasso regression model predicts the prepayment rate for the filtered data.
This integration ensures that predictions are made efficiently, leveraging both models for better accuracy.

### Features

- User-friendly input form for essential mortgage details including `Credit Score`, `Loan-to-Value Ratio`, `Months Since Origination`, and other further features
- Generates predictions:
  - Classification: Determines the risk level 
  - Regression: Estimates the likelihood of prepayment as a percentage
This web application provides real-time feedback on prediction process duration while featuring an easy-to-navigate and visually appealing interface.


###  Deployment via Flask :
- A **Flask web application** is used to deploy the pipeline.
- The Flask app loads the pre-trained models on startup using `joblib` and exposes a `/predict` endpoint to serve predictions.
New data is sent to this endpoint, processed through the pipeline, and predictions are returned in real-time.
The pipeline successfully integrates both classification and regression models to predict mortgage loan delinquency and prepayment rates. With deployment in a Flask app, this pipeline can make real-time predictions and provide meaningful insights.


### Tools :
- Backend: Flask with python libraries
- Frontend: HTML and css for styling
- Machine Learning libraries: Scikit-learn, Pandas, NumPy
- Deployment: Flask
- aws : as a cloud platform for feployment 

### AWS Deployment :
The Flask web application is deployed on AWS Elastic Beanstalk, ensuring scalability and ease of management. The deployment process involves creating an S3 bucket for storing static files and media, Dockerizing the Flask API for consistency across environments, and using Elastic Beanstalk to manage the application infrastructure. AWS Elastic Beanstalk automatically handles the deployment, scaling, and monitoring of the application. SSL certificates for secure communication are configured using AWS Certificate Manager (ACM), while Route 53 manages the domain.

For continuous monitoring and scaling, AWS CloudWatch is implemented, and the application can scale automatically to handle varying loads. This setup ensures the application remains resilient and performs optimally during peak usage.

#### deployment details:  
1. Connect to Your EC2 Instance  
Use the SSH command below to connect to your EC2 instance. Replace <key> with your .pem key file name and <my-instance> with your instance's public IP address.  
```bash  ssh -i "<key>.pem" ubuntu@<my-instance>  ``` 

2. Update and Upgrade System Packages  
Update and upgrade your EC2 instance's packages:  
```bash sudo apt update -y && sudo apt upgrade -y  ```

3. Install Docker  
Install Docker to run your application in a container:  
```bash sudo apt install docker.io  ```

4. Clone the Project Repository  
Clone the GitHub repository for this project using:  
```bash sudo git clone <project repository>  ```
Replace <project repository> with your actual repository URL.  

5. Adjust Security Group Settings  
Update your EC2 instance's security group to allow traffic on port 5000:  
Port Range: 5000  
Protocol: TCP  
Source: 0.0.0.0/0  

6. Run the Docker Container  
Start the Docker container for the project. Replace <project-name> with your Docker image name:  
```bash sudo docker run -d -p 5000:5000 <project-name>  ```
Now your Flask web application should be live and accessible at http://<my-instance>:5000.  

My deployment link : http://ec2-13-60-3-130.eu-north-1.compute.amazonaws.com:5000  (this link is available temporary cause of AWS cost )

![Uploading Screenshot 2024-09-25 181543.png…]()


### conclusion : 
Finally, users can interact with the web app interface by inputting their own feature values to make predictions. By providing the relevant loan attributes through the app, users can receive real-time predictions on whether a loan will become delinquent (via the GBM model) and the expected prepayment rate (via the Lasso regression model). This makes the app accessible for end-users to explore predictions interactively.
