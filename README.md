# ISHIP-PROJECT
## Deploy a website using multiple AWS services.
### Set Up AWS Account:
•	Sign in to AWS Management Console or create a new AWS account.
### Set Up VPC:
•	Create a VPC in the AWS Management Console
<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/1.jpeg" width="800" height="500">
</p>
•	Configure subnets (public and private as needed).
<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/2.jpeg" width="800" height="500">
</p>
•	Set up an Internet Gateway and attach it to the VPC.
<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/3.jpeg" width="800" height="500">
</p>
•	Configure Route Tables to route traffic between subnets and to the Internet Gateway.
<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/4.jpeg" width="800" height="500">
</p>

### Launch EC2 Instance:

•	Go to EC2 Dashboard and select "Launch Instance."

•	Choose an Amazon Machine Image (AMI) suitable for your website (e.g., Ubuntu, Amazon Linux).

•	Select an instance type based on your requirements.

•	Configure instance details, ensuring it’s launched in the correct VPC and subnet.

•	Add storage if needed.

•	Tag your instance for easy identification.

•	Configure security groups (allow inbound traffic on HTTP/HTTPS ports, typically 80/443).

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/5.jpeg" width="800" height="500">
</p>


### Set Up Key Pair:

•	Create or use an existing key pair for SSH access to the instance.

•	Download the .pem file and keep it secure.

### Launch Instance and Access:

•	Review and launch the instance.

•	Use the key pair to SSH into the instance (e.g., ssh -i your-key.pem ec2-user@your-instance-public-ip).


### Configure Web Server:
•	Install web server software (e.g., Apache, Nginx) on your EC2 instance.

•	Upload your website files to the server.

### Test Website:

•	Access your website using the public IP address or Elastic IP assigned to your instance.

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/6.jpeg" width="800" height="500">
</p>

•	Ensure it’s functioning correctly and accessible from the internet.

## Create an Elastic Beanstalk Application:

•	Open AWS Elastic Beanstalk Console.

•	Click “Create Application” and provide application name and platform details.

## Create an Environment:

•	Choose “Create a new environment” and select the environment type (e.g., Web Server, Worker).

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/7.png" width="800" height="500">
</p>

•	Configure environment settings (instance type, scaling, etc.).

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/8.png" width="800" height="500">
</p>

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/9.png" width="800" height="500">
</p>

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/10.png" width="800" height="500">
</p>

### Deploy Your Application:

•	Click “Upload and Deploy” to upload your application’s code package (zip, war, etc.).

•	You can also use the AWS CLI with eb create and eb deploy commands.

## Access Your Website:

•	After deployment, find your application URL in the Elastic Beanstalk Console and test your website.

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/11.png" width="800" height="500">
</p>

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/12.png" width="800" height="500">
</p>

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/13.png" width="800" height="500">
</p>

### Create an S3 Bucket:

•	Go to the S3 Console.

•	Click “Create bucket” and provide a unique name and region.

•	Disable "Block all public access" in permissions settings to allow public access.

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/14.png" width="800" height="500">
</p>

### Upload Website Files:

•	Click on your S3 bucket.

•	Click “Upload” and add your website files (HTML, CSS, JS, etc.).

•	Ensure the files are uploaded to the root or appropriate folder.

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/15.png" width="800" height="500">
</p>

### Configure Bucket for Website Hosting:

•	Go to the bucket properties.

•	Under "Static website hosting", enable it and specify the index document (e.g., index.html).

•	Optionally, specify an error document (e.g., 404.html).

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/16.png" width="800" height="500">
</p>

### Access Your Website:

•	Obtain the S3 website endpoint from the bucket properties.

•	Access your website via the endpoint URL.

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/16.png" width="800" height="500">
</p>

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/17.png" width="800" height="500">
</p>

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/18.png" width="800" height="500">
</p>

<p align="center">
  <img src="https://github.com/mrkiranilla/ISHIP-PROJECT/blob/main/ISHIP-IMAGES/19.png" width="800" height="500">
</p>
















