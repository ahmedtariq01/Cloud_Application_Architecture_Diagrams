## Architection Design Description:

<p align="justify">Suppose there are 10 files uploading to S3 bucket each day. For each file received on cloud storage, you have a mechanism to process the file. During the processing, your code parses the text and to do the further processing. For example, in the following text: “Hello World and Hello There”, your code should be able to say that "hello" has been used twice, "world" has occurred once and so on. Then it will store the results in some storage and email to developers after successful processing.
</p>

##  Architecture Diagram:

### Process files on S3 and email the results Architecture Diagram
<div align="center">
   <div align="center">
    <img src="Architecture_Diagram/Process_S3Files_and_NotificationAlerts.jpg" width='700'/>
   </div>
</div>
</br>



<p align="justify">To create an application that process the files from S3 and email the results to developers, you can follow these steps:</p>
<ol align="justify">   
<li>Create an S3 bucket providing a unique name for the bucket, specifying the region and upload the files to the bucket.</li>
<li>Create a Lambda function that will be triggered using S3 Event notification when a file is uploaded to the S3 bucket. </li>
<li>The Lambda function will process the file data and store the results in database.</li>
<li>Create an SNS topic and subscribe to the topic. The Lambda function will publish the results to the SNS topic.</li>
<li>SNS will send the email to the subscribed email address.</li>
<li>Test the code by uploading sample files to the S3 bucket, and then verify that the results are stored in the database and emailed as expected by checking the email and the database.</li>
</ol>
<p align="justify">By following these steps, you will be able to create an application that process the files from S3 and email the results to developers.</p>

