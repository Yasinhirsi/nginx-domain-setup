## Step-by-Step Setup

1. **Registered domain** on Cloudflare:
   - Chose `yasinhirsi.com` and registered it using Cloudflare's domain registration service
   - Used Cloudflare's DNS management to control records

2. **Launched an EC2 instance** on AWS:
   - Chose **Ubuntu 24.04 LTS** as the base OS
   - Used the **t2.micro** instance type (eligible for free tier)
   - Created and downloaded a new key pair for SSH access
   - Configured security group to allow:
     - **Port 22 (SSH)** — for terminal access
     - **Port 80 (HTTP)** — for web traffic

3. **Installed NGINX** on the EC2 instance:
   ```bash
   sudo apt update
   sudo apt install nginx -y
Verified NGINX was running by visiting the EC2 public IP in a browser

4. **Set up DNS in Cloudflare:**
   - Created an A record pointing nginx.yasinhirsi.com to the EC2 public IPv4 address
   - Configured the record as DNS only (proxy disabled)

5. **Tested the setup:**
   - Opened http://nginx.yasinhirsi.com in a browser
   - Confirmed the default "Welcome to NGINX" page was served successfull


