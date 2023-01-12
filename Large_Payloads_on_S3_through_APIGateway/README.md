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
<li>Set up an Amazon S3 bucket to store the website pages. The bucket should be configured to host a static website.

<li>Set up an Amazon EC2 instance to run the static calculations required by the website. The EC2 instance should be configured to run the necessary software and libraries for the calculations.

<li>Set up an Amazon API Gateway to handle requests to the website and trigger corresponding Lambda functions to handle the requests.

<li>Set up Lambda functions to handle the requests from the API Gateway and perform the necessary actions. For example, a Lambda function can be triggered when an API request is received to retrieve data from the EC2 instance and return it to the website.

<li>Set up an Amazon CloudWatch alarm to monitor the number of API calls received by the API Gateway. The alarm can be configured to send a notification when the number of API calls exceeds a certain threshold.

<li>To enable continuous delivery, you can set up a continuous integration (CI) tool such as Jenkins or AWS CodePipeline. The CI tool can be configured to automatically build, test, and deploy the website to the S3 bucket whenever code changes are made to the website's source code.

<li>To enable continuous deployment, you can set up a deployment pipeline in the CI tool. The deployment pipeline can be configured to automatically deploy the website to the S3 bucket and update the API Gateway and Lambda functions when new code is pushed to the repository.

</ol>
<p align="justify">By following these steps, you can create an end-to-end CI/CD delivery pipeline for a website on AWS that uses EC2 instances for static calculations, S3 for website pages, API Gateway and Lambda triggers, and CloudWatch alarms to monitor the number of API calls received.</p>

