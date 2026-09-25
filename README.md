# AWS DevOps Web Server Project

This is a mini AWS DevOps project I built to understand how a web server is deployed and accessed through AWS networking.

I created a custom VPC, configured public and private subnets, set up routing and network security, and deployed an Nginx web server on an Amazon Linux EC2 instance.

## What I built

- Created a custom VPC with CIDR `10.0.0.0/16`
- Created 2 public and 2 private subnets
- Configured route tables and an Internet Gateway
- Created a Security Group for SSH and HTTP access
- Created and associated a custom Network ACL
- Launched an Amazon Linux 2023 EC2 instance
- Connected to the server using SSH
- Installed and configured Nginx
- Created a simple custom webpage and hosted it using Nginx

## Testing

I tested the setup from both the EC2 server and my local browser.

Some of the checks I performed:

- Checked the EC2 network interface and private IP
- Checked the Linux routing table
- Tested DNS resolution
- Tested outbound internet access using `curl`
- Tested the Nginx server locally
- Accessed the website using the EC2 public IP
- Checked Nginx access and error logs
- Verified that Nginx starts automatically after reboot

## Troubleshooting

While testing the server, `ping 8.8.8.8` did not receive any replies.

However, HTTPS requests using `curl` worked successfully and the website was accessible from my browser. This helped me understand that a failed ping does not necessarily mean that the server has no internet connectivity.

## Tools I used

- AWS
- Amazon EC2
- Amazon VPC
- Linux
- Nginx
- SSH
- Git
- PuTTY / PuTTYgen

## What I learned

Through this project I got hands-on practice with AWS VPC networking, EC2, Linux server administration, routing, Security Groups, Network ACLs, Nginx and basic network troubleshooting.
