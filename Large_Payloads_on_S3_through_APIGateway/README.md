## Architection Design Description:

<p align="justify">What if we have a 15MB file that we have to upload on S3 using API gateway. 
We have the limitation that our API gateway has the maximum payload capacity of 10MB. How will you solve this problem?</p>

##  Architecture Diagram:

### Uploading Large Payloads on S3 Architecture Diagram
<div align="center">
   <div align="center">
    <img src="Architecture_Diagram/Uploading_Large_Payloads_on_S3.jpg" width='700'/>
   </div>
</div>
</br>



<p align="justify">To create an application to allow user to upload large payloads on S3, you can follow these steps:</p>
<ol align="justify">   
<li>Create an S3 bucket using the AWS CDK in Python. The S3 bucket should be configured to allow public access to the objects it contains. The S3 bucket should also be configured to allow the API Gateway to access the objects it contains.</li>

<li>Create an API Gateway REST API with a POST method that can handle requests with a payload size of up to 10 MB. The API Gateway should be configured to trigger a Lambda function when a request is received.</li>

<li>Create the first Lambda function using the AWS CDK in Python, which is responsible for generating a presigned URL for the client to use to upload a file to the S3 bucket. The Lambda function should be configured to allow the API Gateway to invoke it.</li>

<li>Create the second Lambda function using the AWS CDK in Python, which is responsible for generating a presigned URL for the client to use to download a file from the S3 bucket. The Lambda function should be configured to allow the API Gateway to invoke it.</li>

<li>Configure the S3 bucket to trigger the second Lambda function whenever a new object is created. The Lambda function should be configured to allow the S3 bucket to invoke it.</li>

<li>Configure the API Gateway to trigger the first Lambda function when a request is received. The Lambda function should be configured to allow the API Gateway to invoke it.</li>

<li>Test the project by using the POST method to request a presigned URL and then uploading a file to the S3 bucket.</li>

</ol>
<p align="justify">By following these steps, you will be able to create an application to allow user to upload large payloads on S3.</p>

