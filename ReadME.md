This sample project covers:
<ul>
<li>Hosting S3 Static Website</li>
<li>Createing CloudFront OAC (Origin Access Control or OriginAccess Identity) distribution</li>
<li>Configuring continous deployment from github to S3 Bucket using GitHub Actions</li>
<li>Using API Gateway and Lambda Function to display the no. of visitors </li>
<li>Using API Gateway and Lambda Function to forward the ContactUs Form details to an email using SES/SNS</li>
</ul>

<b>Important:</b>
For CloudFront distribution, after creating CloudFront distribution you must create a bucket policy to give permission to CloudFront
![image](https://user-images.githubusercontent.com/43560747/210114675-dbec2f09-e4b3-406d-95d3-a80bbfd5c954.png)
</i>
For CD from GitHub to AWS, Add your AWS Access Key and Secret to your project repo
