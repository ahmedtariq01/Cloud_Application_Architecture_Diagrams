## Architection Design Description:

<p align="justify"> The client needs a notification system that sends updates to administrators, users and clients/users. The system should be AWS-based, cost-effective, scalable, secure, handle high volume of notifications, easy to manage and maintain. The client needs recommendations for the best AWS service(s) to implement this system. Which AWS service(s) would you recommend for this system?</p>


##  Architecture Diagram:

### WebApp HealthCheck Architecture Diagram
<div align="center">
   <div align="center">
    <img src="Architecture_Diagram/Notification_System.jpg" width='700'/>
   </div>
</div>
</br>



<p align="justify">To create a notification system for your application, you can follow these steps:</p>
<ol align="justify">   
<li>Create AWS CloudWatch to monitor the health of your application.</li>
<li>Create AWS Systems Manager to collect and analyze operational data to monitor the status and performance of the application.</li>
<li>Create a Lambda function to fetch the data from AWS CloudWatch and AWS Systems Manager and process it and generate reports.</li>
<li>Create AWS SES to send the reports to the users and admins via email.</li>
<li>Configure a CloudWatch Event to trigger the Lambda function at a regular interval.</li>
</ol>
<p align="justify">By following these steps, you will be able to notification system for your applicationp>

