# Week 1: AWS Static Website
## Progress
- Starting my Cloud Support journey!
- Created a new professional email (HussainA.Cloud@gmail.com) for roadmap accounts.
- Set up AWS Free Tier account to begin cloud projects.
- Configured LinkedIn profile with Co-Founder experience at HHCommerce LLC (2017–2023), focusing on e-commerce and wholesale retail.
- Uploaded resume to LinkedIn, highlighting technical support and automation skills.
- Joined r/aws community on Reddit using existing account for networking.
- Tested draw.io by creating an EC2-S3 diagram, preparing for the Week 1 architecture diagram.
- Finished AWS Cloud Practitioner Essentials Module 1 and aced the quiz (3/3 correct).
- Set $5/month budget alert in AWS to manage costs, with thresholds at 80% ($4) and 100% ($5).
- Completed AWS Cloud Practitioner Essentials Module 2 (compute services: EKS, ECS, SNS, SQS) and took the quiz.
- Explored AWS Console (EC2, S3, VPC)
- Read AWS EC2 Lab intro to prepare for instance setup.
- Launched an EC2 instance (Amazon Linux 2, t2.micro, Instance ID: [i-0bf4f1fd1fa058314], Public DNS: ec2-3-133-89-50.us-east-2.compute.amazonaws.com), saved .pem key securely, and connected via SSH on Windows.
- Created S3 test bucket (week1-test-bucket-hussain) and uploaded test.txt for Week 1 project.
## Friday, May 30, 2025: EC2 Static Website Setup
- Installed Apache on EC2 instance (Amazon Linux 2, t2.micro, Public DNS: ec2-3-133-89-50.us-east-2.compute.amazonaws.com) using `sudo yum install httpd -y`, started and enabled with `systemctl`, verified with `curl localhost`.
- Deployed website files: Downloaded test.txt from S3, uploaded to /var/www/html/, created index.html ("Hello World" page with link to test.txt), set permissions, tested with `curl localhost`.
- Configured EC2 security group: Added HTTP rule (port 80, source: Anywhere), tested website in browser (`http://ec2-3-133-89-50.us-east-2.compute.amazonaws.com`), confirmed test.txt link worked.
- Stopped EC2 instance to pause Free Tier usage.
