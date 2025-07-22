Step-by-Step Setup

Registered domain at Cloudflare: yasinhirsi.com

Launched EC2 Ubuntu 24.04 instance via AWS

Installed NGINX on EC2: sudo apt update

   sudo apt install nginx -y

Verified NGINX page at EC2 public IP

Created A record on Cloudflare:

Type: A

Name: nginx

IP: 13.41.157.242

Confirmed site live at: http://nginx.yasinhirsi.com


