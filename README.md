# Grocery-website-


Welcome to the Grocery Website repository! This repository contains the codebase and assets for an innovative online grocery shopping platform. Below, you'll find an overview of how Amazon S3, Amazon EC2 with Nginx, and Elastic IP have been seamlessly integrated into this project.

**Amazon S3 Bucket Utilization:**
To efficiently store and deliver static assets such as images, CSS files, and JavaScript resources, an Amazon S3 bucket has been employed. The bucket is configured to allow public access to these assets through a modified bucket policy. This enables rapid content delivery and optimizes website performance.

**Amazon EC2 with Nginx:**
Amazon EC2 instances, powered by Nginx, serve as the dynamic core of the Grocery Website. They manage user requests, handle application logic, and connect to the database. Nginx ensures load balancing and efficient routing of traffic among instances, optimizing responsiveness and uptime.

**Elastic IP Address:**
An Elastic IP address has been assigned to the EC2 instances to provide a consistent public IP address. This prevents disruption caused by instance restarts or reboots, ensuring that the website remains reliably accessible.

**Commands for Deployment:**

1. **Amazon S3 Bucket Configuration:**
   - Create an S3 bucket: `aws s3api create-bucket --bucket your-bucket-name --region your-region`
   - Upload files to the bucket: `aws s3 cp local-file s3://your-bucket-name/`
   - Modify bucket policy for public access: Update the policy JSON to allow public access and apply it using the AWS Management Console or `aws s3api put-bucket-policy --bucket your-bucket-name --policy file://bucket-policy.json`

2. **Amazon EC2 Instance Setup:**
   - Launch an EC2 instance: Use the AWS Management Console or `aws ec2 run-instances --image-id your-ami-id --instance-type your-instance-type`
   - SSH into the instance: `ssh -i your-key-file.pem ec2-user@your-ec2-public-ip`

3. **Nginx Installation and Configuration:**
   - Install Nginx: `sudo yum install nginx`
   - Configure Nginx: Edit `/etc/nginx/nginx.conf` and `/etc/nginx/conf.d/default.conf` for server block settings
   - Reload Nginx: `sudo systemctl reload nginx`

4. **Elastic IP Association:**
   - Allocate an Elastic IP: Use the AWS Management Console or `aws ec2 allocate-address`
   - Associate the Elastic IP: `aws ec2 associate-address --instance-id your-instance-id --public-ip your-elastic-ip`

By blending these AWS services and components, we've crafted a sophisticated and high-performance Grocery Website that offers an engaging and efficient shopping experience. Feel free to explore and contribute to this repository, and let's continue enhancing the future of online grocery shopping together!

Downloading and Setting Up the Project:

Download the Repository:

Click the "Download ZIP" button on this repository's GitHub page.
Extract the ZIP folder to a location on your local system.
Configurations:

Open the appropriate files to set up environment variables (such as database credentials) according to the provided documentation.
Website Deployment:

Follow the documentation to upload static assets to your Amazon S3 bucket.
Configure and launch an Amazon EC2 instance, and install Nginx as directed.
Domain Configuration (Optional):

If you have a domain, configure the DNS settings to point to the Elastic IP address.
By following these steps, you'll successfully deploy the Grocery Website on your local system. Feel free to explore and contribute to this repository, and let's continue enhancing the future of online grocery shopping together!
