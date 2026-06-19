# DecodeLabs-Project-2-server-commander

## Project Title
AWS EC2 Linux Instance Launch + Apache Web Server Deployment

## Description
Is project mein maine AWS EC2 par Amazon Linux 2023 instance launch kiya. Instance type t3.micro use kiya jo Free Tier eligible hai. Security group mein SSH, HTTP, HTTPS ports open kiye. SSH se connect karke Apache web server install kiya aur public IP 16.171.196.130 par custom page verify kiya: "Welcome to DecodeLabs: Mission Accomplished"

## Steps Performed
1. AWS Console login karke EC2 Dashboard open kiya
2. Launch Instance par click kiya
3. Name rakha: Server-Commander-01
4. AMI select ki: Amazon Linux 2023 - Free Tier Eligible
5. Instance type select kiya: t3.micro - 2 vCPU, 1 GiB Memory
6. Key pair banayi: server-commander-key.pem
7. Network settings: Auto-assign Public IP Enabled
8. Security Group banaya: launch-wizard-1
   - SSH port 22 - Anywhere 0.0.0.0/0 allow
   - HTTP port 80 - Anywhere allow
   - HTTPS port 443 - Anywhere allow
9. Storage: 8 GiB gp3 Root volume
10. Instance launch kiya - Instance ID: i-0bb9ed19b34518ca0
11. Public IPv4 note kiya: 16.171.196.130
12. SSH command: ssh -i server-commander-key.pem ec2-user@16.171.196.130
13. Apache install: sudo dnf install httpd -y
14. Apache start: sudo systemctl start httpd
15. Apache enable: sudo systemctl enable httpd
16. Custom page deploy kiya aur browser mein verify kiya: http://16.171.196.130

## Screenshots

### 1. Launch Instance Page
Name: Server-Commander-01, AMI: Amazon Linux 2023
![Launch Instance](WhatsApp%20Image%202026-06-19%20at%204.56.31%20PM.jpeg)

### 2. Instance Type Selection
t3.micro Free Tier Eligible
![Instance Type](WhatsApp%20Image%202026-06-19%20at%204.56.31%20PM%20(1).jpeg)

### 3. Key Pair + Security Group Settings
server-commander-key, HTTP/HTTPS/SSH allowed
![Security Group](WhatsApp%20Image%202026-06-19%20at%204.56.31%20PM%20(2).jpeg)

### 4. EC2 Dashboard Running
Instance i-0bb9ed19b34518ca0 status Running
![Dashboard](WhatsApp%20Image%202026-06-19%20at%204.56.32%20PM.jpeg)

### 5. Instance Details Public IP
Public IP 16.171.196.130 visible
![Public IP](WhatsApp%20Image%202026-06-19%20at%204.56.32%20PM%20(1).jpeg)

### 6. Apache Mission Accomplished Page
Custom page "Welcome to DecodeLabs: Mission Accomplished" verified on http://16.171.196.130
![Apache Mission Accomplished](project%202.PNG)

## AWS Resources Created
- EC2 Instance: i-0bb9ed19b34518ca0
- Instance Type: t3.micro
- AMI: Amazon Linux 2023
- Key Pair: server-commander-key.pem
- Security Group: launch-wizard-1 with ports 22, 80, 443
- Public IP: 16.171.196.130
- Storage: 8 GiB gp3

## Learnings
Is project se maine seekha ke EC2 instance kaise launch karte hain, security group kaise configure karte hain web server ke liye, SSH se Linux server mein kaise connect karte hain, Amazon Linux 2023 par Apache web server kaise install karte hain, aur custom HTML page kaise deploy karte hain.
