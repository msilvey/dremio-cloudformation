# dremio-cloudformation
A CloudFormation template to load up an instance of Dremio on Ubuntu 18.04.1 LTS.

Some quick considerations:
--------------------------
- This is a small single instance deployment. 
- This template creates a new VPC and a subnet in the 'c' AZ of the given region.
- The software is built with the OSS-only option set. Oracle/MS SQL Server integration will not work.
- The SSL/TLS options are disabled. All traffic to the Web UI is in the clear.

Usage:
------
Open a web browser, login to your AWS account and navigate to:
- https://console.aws.amazon.com/cloudformation/home
- Click 'Create Stack' and select 'Upload a template to Amazon S3', then click 'Browse' and navigate to the JSON template file.
- Click 'Next', give your stack a name, select a key, click 'Next'.
- Click on 'I acknowledge that AWS CloudFormation might create IAM resources.' then click 'Next' again and off you go.
