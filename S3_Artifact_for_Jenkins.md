https://github.com/ValaxyTech/DevOpsDemos/blob/master/Jenkins/S3_Artifact_for_Jenkins.md
Prerequisites
Create Jenkins Server Jenkins server Get Help here

Setup steps
Create a S3 bucket to store artifacts
S3 --> Create bucket

Bucket name: valaxy-s3-artifact 
Region: Singapore
Create new IAM role with "S3 full access" and assign it to jenkins server
IAM --> Create role --> EC2

Permission: AmazonS3FullAccess 
Tags: key - Name, Value - S3FullAccess Role 
name: S3_Full_Access
Install "S3 Publisher" plugin on Jenkins
Manage Jenkins --> Manage Plugins --> Availabe --> S3 publisher

Configure S3 profile on Jenkins
Manage Jenkins --> Configure Systems --> Amazon S3 profiles

Profile name : s3-artifact-repository 
Use IAM Role : chose
Create a job to store artifacts under S3
