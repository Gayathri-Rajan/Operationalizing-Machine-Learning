# Operationalizing Machine Learning

In this project Automated ML is used to find the best model. The model is then deployed. The application insigts are enabled in order to obtain importat information.In the later stages, a pipeline is also created and it is published. The dataset used for this project is Bank Marketing dataset. These are the steps that are followed to complete the project.

1.Authentication

2.Automated ML Experiment

3.Deploy the best model

4.Enable logging

5.Swagger Documentation

6.Consume model endpoints

7.Create and publish a pipeline



## Architectural Diagram
<img src="./Screenshots/bloc.jpg" />

## Key Steps

1. Authentication

A service principal should be created for authetication. Since I did the project on the Lab provided with the course, it is done.

2.Auto ML Experiment

The Bank Marketing Dataset needs to be uploaded and a compute cluster  Standard_DS12_V2 is configured with 1 as the minimum umber of nodes. Then an Auto ML experiment is created to find the best model. The follwing screeshots shows the step.

### Dataset
The screenshot shows that the Bank Maeketing dataset has been uploaded
<img src="./Screenshots/registered dataset.jpg" />

### Autom ML Experiment Completed
The AutoML experiment is completed. It shows the best model and the other models.
<img src="./Screenshots/expt completed.jpg" />

### Auto ML Models
This shows the list of different models through which the AutoML experiment has run through
<img src="./Screenshots/automl run.jpg" />

### Best Model
The best Model obtained through the AutoML experiment is Voting Ensemble. The accuracy of the model is 0.91806.
<img src="./Screenshots/best model.jpg" />

3. Deploy the best model
The best model, in this case, Voting Ensemble is deployed using Azure Container Instance(ACI) and we make sure that the deployment status is healthy.

### Deploying the best model
The model - Voting Ensemble is deployed using Azure Container Instances. The authentication is enabled.
<img src="./Screenshots/best model deploy.jpg" />

### Deployed Status- Healthy
This screenshot shows that the model has been deployed and thet status is healthy
<img src="./Screenshots/deployed best model.jpg" />

4. Enable Logging 
Once the best model is deployed, we have to enable logging using the python file logs.py. The application insights are made true for the deployed endpoints and to retrieve the log. The following screenshots shows the logs.

### Running logs.py script
We choose the best model for deployment and enable "Authentication" while deploying the model using Azure Container Instance (ACI). The executed code in logs.py enables Application Insights. "Application Insights enabled" is disabled before executing logs.py.
<img src="./Screenshots/logs.py1.jpg" />
<img src="./Screenshots/logs.py2.jpg" />

### Applications inisghts enabled to True
The screenshot show that the Applicatio Insights has turned to True.
<img src="./Screenshots/apps insights true.jpg" />

5.Swagger Documentation 
In this step, swagger container is deployed in order to view the swagger documetation. For this the swagger.json file is downloaded. The swagger.sh and serve.py file is run. All these files should be in the same folder. The GET and POST request could be observed in the swagger UI. The below screenshots show the swagger documentation.

### Running swagger.sh file
The port number is updated and the swagger.sh file is executed.
<img src="./Screenshots/swager.sh1.jpg" />
<img src="./Screenshots/swagger.sh3.jpg" />

### Running serve.py file
After executing swagger.sh file, the serve.py python file is executed.
<img src="./Screenshots/serve.py.jpg" />

### Swagger documentation
The swagger UI is shown in the follwoing screeshot
<img src="./Screenshots/swagger.jpg" />

### GET request
<img src="./Screenshots/get.jpg" />

### POST request
POST request accepts json. The sample data tells us what type of data is being accepted. 
<img src="./Screenshots/post.jpg" />
<img src="./Screenshots/post2.jpg" />

6. Consume Model Endpoints
Since the model is deployed, we can interact with the trained model. The endpoint.py file is used to show that the endpoint is consumed. The below screenshot shows the response that endpoint.py returns.

### Running endpoints.py file
After swagger documentation, the endpoints.py file is executed. The screenshot shows the output.
<img src="./Screenshots/enpoint.py.jpg" />

7. Create and Publish a Pipeline
In this step a pipeline is created. Jupyter notebook is used for AutoML run. config.json file is downloaded. After setting the pipeline, the pipeline is run and late it is published which could be observed under pipline endpoints. The follwoing screenshots shows the creation and publishing of the pipleine.

### Pipeline created 
The pipeline is created.
<img src="./Screenshots/pipeline running.jpg" />

### Pipeline Endpoint
The screenshot shows the pipleine endpoint
<img src="./Screenshots/pipeline endpoint.jpg" />

### Pipeline Completed
The pipeline is completed
<img src="./Screenshots/pipeline completed.jpg" />

### Published Pipeline Overiew
<img src="./Screenshots/rest edpoitactive.jpg" />

### RunDetails Widget
<img src="./Screenshots/rundetailswidget.jpg" />

### Scheduled run
<img src="./Screenshots/scheduled run.jpg" />

## Screen Recording
Link to the video of the project. [Video Link](https://youtu.be/uJwDk4LoBVI)

## Future Improvements
1. More data could be collected. This would help to improve the model accuracy.
2. Feature engineering could be done in order to get better understading of the data.

