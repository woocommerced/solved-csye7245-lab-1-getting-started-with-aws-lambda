Download Link: https://assignmentchef.com/product/solved-csye7245-lab-1-getting-started-with-aws-lambda
<br>
This lab demonstrated the implementation of AWS CLI and other services like IAM, Amazon S3, comprehend and lambda.

<strong>Amazon Web Services (AWS)</strong> provides computing resources and services that you can use to build applications within minutes at <strong>pay-as-you-go pricing</strong>. You can run nearly anything on AWS that you would run on physical hardware: websites, applications, databases, mobile apps, email campaigns, distributed data analysis, media storage, and private networks. The services they provide are designed to work together so that we can build complete solutions. There are currently dozens of services, with more being added each year. AWS is readily distinguished from other vendors because it is <strong>flexible, cost-effective, scalable, elastic </strong>and <strong>secure</strong>.

<h1>Experiment setup</h1>

<strong><u>Prerequisites:</u></strong>

<ol>

 <li><strong>Creating an AWS account</strong></li>

</ol>

<strong>       </strong>Creating an AWS account <a href="https://aws.amazon.com/console/">here </a>

<ol start="2">

 <li><strong>Configuring AWS CLI</strong></li>

</ol>

<strong>       </strong>Download AWS CLI from <a href="https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html">here</a>

<strong>Configuring AWS on our system</strong>

<ul>

 <li>Open cmd</li>

 <li>aws configure</li>

 <li>Enter Access Key and Secret Access Key</li>

 <li>Keep region and file format blank</li>

</ul>

<ol start="3">

 <li><strong>Starting with IAM ( Identity Access Management )</strong></li>

</ol>

<ul>

 <li>Always login as a root user to have all the privileges and access to all services</li>

 <li>Generate Access and Secret Access keys. Download it for future reference</li>

</ul>

<ol start="4">

 <li><strong>Creating a virtual environment</strong></li>

</ol>

Virtual environment helps us to create an isolated environment for all Python projects. Each project can thus have it’s own dependencies.

mkdir first-lambda

python3 -m venv tutorial-env




Activate the virtual environment →   /Scripts/activate.bat




Install all the required packages in this virtual env – first-lambda




pip3 install Faker

pip3 install boto3

<strong> </strong>

<h1>Test Results</h1>

<strong>Creating a S3 bucket</strong>

<strong>Amazon S3</strong> – <strong>a simple storage service</strong> is a scalable, high-speed, web-based cloud storage service. This service is designed for online backup and archiving of data and applications on Amazon Web Services (AWS).

<strong>     </strong>Ensure below mentioned rules while creating any S3 bucket:

<ul>

 <li>Block all public access</li>

 <li>Disable bucket versioning</li>

 <li>Disable encryption</li>

</ul>

<h1>Use Cases</h1>

Let’s consider a simple use case to upload fake data in <strong>S3 bucket</strong> using Python packages like Faker and Boto3

<strong>Faker</strong>: A python package to generate fake data

<strong>Boto3</strong>: Boto3 is a Amazon Web Services (AWS) Software Development Kit (SDK) for Python which allows Python developers to write software that makes use of services like Amazon S3 and Amazon EC2

<ul>

 <li><strong>py</strong></li>

</ul>

Python script to generate some fake data using Faker and upload to your S3 Bucket

S3 bucket<strong> priyankabucket-1</strong> created and fake csv uploaded in the respective bucket.

<ul>

 <li><strong>py</strong></li>

</ul>

Download the generated csv file from S3 bucket to your local environment.

<ul>

 <li><strong>py</strong></li>

</ul>

Using AWS <strong>comprehend </strong>service to detect sentiments.  <strong>Comprehend </strong>is used for sentimental     analysis. Consider the below mentioned use case to understand the concept of sentiment analysis using  comprehend:

<strong>   </strong>   <strong> </strong><strong>miserable —&gt; Negative sentiment</strong>

<strong>  </strong>Every word has a sentiment score viz. <strong>Mixed, Negative, Neutral </strong>and <strong>Positive</strong>.

<strong>  happy —&gt; Positive sentiment</strong>

<h1>Lambda-serverless-py</h1>

<strong>AWS Lambda</strong> is a <strong>serverless </strong>compute service that runs your code in response to events. It lets you run code without provisioning or managing servers. Lambda runs your code only when needed and scales automatically, from a few requests per day to thousands per second.

<strong>Creating a basic Lambda function</strong>

<strong>Create an IAM Role</strong>

Creating a lambda role named ‘lambda_basic_execution’ with following privileges:

<ul>

 <li>Lambda basic execution</li>

 <li>Amazon S3 full access</li>

 <li>Amazon DynamoDB full access</li>

</ul>

Everything should be under <strong>lambda_handler</strong> function . Rename it as lambda_h by making changes in runtime settings.

<strong>Executing the ‘test-lambda function’</strong>

<strong>Deploying Lambda function</strong>

<ul>

 <li>Creating a virtual environment</li>

 <li>Installing required packages</li>

</ul>

pip3 install python-lambda

pip3 install pandas

<ul>

 <li>Initiating lambda deployment</li>

</ul>

lambda.py init

Three files will be generated viz. <strong>Config.yaml, events.json, service.py</strong>

The <strong>service.py</strong> is the file we will be using. We can edit service.py with our Python code.

<strong>Deploying lambda function</strong>

lambda.py deploy

<strong>Lambda function successfully deployed</strong>










<h1></h1>

<h1>Lessons Learned</h1>




<ol>

 <li>Uploading and downloading fake data using Faker in Amazon S3 bucket using python package like Boto3</li>

 <li>Deploying lambda functions using AWS CLI</li>

 <li>Learnt to use comprehend for sentiment analysis</li>

 <li>Learnt about IAM roles and user permissions in AWS</li>

</ol>







<h1>References</h1>




<a href="https://media.amazonwebservices.com/AWS_Overview.pdf">https://media.amazonwebservices.com/AWS_Overview.pdf</a>




<a href="https://awsdocs.s3.amazonaws.com/gettingstarted/latest/awsgsg-intro.pdf">https://awsdocs.s3.amazonaws.com/gettingstarted/latest/awsgsg-intro.pdf</a>




<a href="https://docs.aws.amazon.com/lambda/latest/dg/welcome.html">https://docs.aws.amazon.com/lambda/latest/dg/welcome.html</a>





