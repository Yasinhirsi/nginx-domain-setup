# NGINX + Custom Domain (Cloudflare + EC2)

## Live Demo
🌍 http://nginx.yasinhirsi.com

<img width="1440" height="900" alt="nginx welcome" src="https://github.com/user-attachments/assets/46561c6f-ccff-4d7b-9d76-e3e0dc0560e6" />


## 📖 What I Did (Detailed Breakdown)
Registered a custom domain

Chose and registered yasinhirsi.com using Cloudflare Domains

Chose Cloudflare for its wholesale pricing and free DNS management

Launched an EC2 instance on AWS

Used the AWS EC2 console to launch an instance

Selected the Ubuntu 24.04 LTS AMI

Chose t2.micro instance type (Free Tier)

Created and downloaded a new SSH key pair (yasin-nginx-key.pem)

Configured security group rules to allow:

Port 22 (SSH) – for terminal access

Port 80 (HTTP) – for web traffic

Accessed the EC2 instance via SSH

Used the .pem key to SSH into the instance:

bash
Copy
Edit
ssh -i ~/.ssh/yasin-nginx-key.pem ubuntu@<public-ip>
Installed and tested NGINX

Ran the following commands on the instance:

bash
Copy
Edit
sudo apt update
sudo apt install nginx -y
Confirmed installation by visiting the EC2 public IP in a browser and seeing the default "Welcome to NGINX" page

Configured DNS using Cloudflare

Logged into the Cloudflare dashboard

Created an A record for nginx.yasinhirsi.com pointing to the EC2 public IPv4 address

Disabled the proxy (set to DNS-only) to allow direct HTTP access

Verified the full setup

Successfully accessed the NGINX welcome page using:
🌍 http://nginx.yasinhirsi.com

Pushed all work to GitHub using SSH

Set up SSH authentication with GitHub using id_ed25519.pub

Changed Git remote to use SSH:

bash
Copy
Edit
git remote set-url origin git@github.com:Yasinhirsi/nginx-domain-setup.git
Committed and pushed the project to GitHub without using HTTPS passwords

