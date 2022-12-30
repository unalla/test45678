Sample project to covers:
<ul>
<li>Hosting S3 Static Website</li>
<li>Createing CloudFront OAC (Origin Access Control or OriginAccess Identity) distribution</li>
<li>Configuring continous deployment from github to S3 Bucket using GitHub Actions</li>
<li>Using API Gateway and Lambda Function to display the no. of visitors </li>
<li>Using API Gateway and Lambda Function to forward the ContactUs Form details to an email using SES/SNS</li>
</ul>

<b>Important:</b>
For CloudFront distribution, after creating CloudFront distribution you must create a bucket policy to give permission to CloudFront
<i>{
    "Version": "2008-10-17",
    "Id": "PolicyForCloudFrontPrivateContent",
    "Statement": [
        {
            "Sid": "AllowCloudFrontServicePrincipal",
            "Effect": "Allow",
            "Principal": {
                "Service": "cloudfront.amazonaws.com"
            },
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::Your Website/*",
            "Condition": {
                "StringEquals": {
                    "AWS:SourceArn": "arn:aws:cloudfront::Your-AccountId:distribution/CloudFront-DistributionName"
                }
            }
        }
    ]
}
</i>
For CD from GitHub to AWS, Add your AWS Access Key and Secret to your project repo
