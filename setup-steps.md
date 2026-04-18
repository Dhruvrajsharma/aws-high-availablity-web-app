## Step 1: VPC Setup

- Created a custom VPC with CIDR block 10.0.0.0/16
- Created 2 public and 2 private subnets across multiple AZs
- Attached Internet Gateway to VPC
- Configured route tables for public access

## Screenshot
See /screenshots/vpc.png


## Step 2: EC2 Setup

- Launched EC2 instance (Amazon Linux 2)
- Installed Apache web server
- Hosted a simple web page
- Enabled HTTP and SSH access via Security Groups

## Screenshot
See /screenshots/ec2.png


## Step 3: Application Load Balancer

- Created Application Load Balancer
- Configured target group
- Registered EC2 instance
- Verified traffic distribution

## Screenshot
See /screenshots/alb.png


## Step 4: Auto Scaling

- Created Launch Template using AMI
- Configured Auto Scaling Group
- Set desired, min, and max instances
- Attached to Load Balancer

## Screenshot
See /screenshots/autoscaling.png

## Step 5: RDS Database Setup

- Created MySQL database using Amazon RDS (Free Tier)
- Deployed inside private subnet for security
- Disabled public access
- Configured security group to allow access only from EC2
- Used managed database for automated backups and maintenance

## Screenshot
See /screenshots/rds.png


## Step 6: CloudWatch Monitoring

- Created CloudWatch alarm for EC2 CPU Utilization
- Set threshold to trigger when CPU exceeds 70%
- Configured monitoring for performance tracking and alerting

## Screenshot
See /screenshots/cloudwatch-alarm.png
