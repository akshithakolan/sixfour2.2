
# Assignment:2

# Static Website Hosting on Amazon S3

End point URL : 
http://swe642hwtwoo.s3-website-us-east-1.amazonaws.com

# Homepage URL, CS Department, Survey Form (S3 Hosted):

CS dept survery form link: 
https://swe642hwtwoo.s3.amazonaws.com/csdeptsurvey.html


### Instructions to Access the Application
Visit the homepage by clicking the S3 URL provided above.
To access the survey form, click on the link provided on the homepage, which directs to the survey form hosted on an EC2 instance.
You can also directly visit the survey form by using the EC2 URL provided.

### S3 hosting
Step-by-Step Procedure: Hosting a Static Website on Amazon S3 
Log in to AWS Console:

Open AWS Management Console and sign in to your account.
Create an S3 Bucket:

Navigate to S3 Service.
Click Create Bucket.
Choose a unique bucket name (e.g., swe642hwone).
Choose the appropriate region (e.g., us-east-2).
Uncheck the Block all public access option, as the website will need to be public.
Click Create Bucket.
Upload Website Files:

Click on your newly created bucket.
Navigate to the Objects tab and click Upload.
Upload your HTML, CSS, and image files, including your index.html (homepage) and other necessary files.
Enable Static Website Hosting:

In the Properties tab of your S3 bucket, scroll down to Static website hosting.
Enable static website hosting.
Set index.html as the Index document.
Set a custom error page (e.g., error.html) if desired.
Note the S3 Endpoint URL (http://swe642hwone.s3-website-us-east-1.amazonaws.com),.
Set Permissions:

Go to the Permissions tab of your S3 bucket.
In Bucket Policy, add the following policy to make the bucket accessible to the public:
```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::swe642hwone/*"
    }
  ]
}
```
Save the bucket policy.
Test Your Website:

Access your static website via the S3 Endpoint URL you noted in step 4.

