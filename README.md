# aws-project2-web-app-
Create an EC2 Instance
 EC2 → Launch Instance.
Choose an Amazon Machine Image (AMI):
Ubuntu Server 20.04 or 22.04 LTS
Select an instance type:
t2.micro (Free Tier eligible)
Create or select an existing key pair for SSH access.
<img width="1919" height="777" alt="Screenshot 2026-02-04 121644" src="https://github.com/user-attachments/assets/75b9d5f2-d9d8-499d-9f01-ab88d468b7f3" />
<img width="1912" height="712" alt="Screenshot 2026-02-04 121724" src="https://github.com/user-attachments/assets/ca831f3e-e6e0-4f8c-b7c0-cabe6847436c" />

Configure Security Groups (Firewall Rules)
Configure the EC2 security group to allow the following inbound traffic:
Protocol
Port
Source
SSH
22
Your IP
HTTP
80
Anywhere (0.0.0.0/0)
<img width="1919" height="755" alt="Screenshot 2026-02-04 121826" src="https://github.com/user-attachments/assets/58f878b7-405e-4d70-bdab-f7bcadc470f6" />

Connect to EC2 Using SSH
<img width="1919" height="786" alt="Screenshot 2026-02-04 122211" src="https://github.com/user-attachments/assets/bce4cfaf-51b1-4430-9154-327d3e533821" />
<img width="1909" height="751" alt="Screenshot 2026-02-04 122224" src="https://github.com/user-attachments/assets/15014374-5bd4-438b-8935-d9ce122b9880" />
<img width="1471" height="746" alt="Screenshot 2026-02-04 122740" src="https://github.com/user-attachments/assets/732c5330-0f3e-4a1e-a571-42807cd06c4f" />

Install and Start Apache2 Web Server
Update the package list:
sudo apt update

Install Apache2:
sudo apt install apache2 -y

Start and enable Apache:
sudo systemctl start apache2
sudo systemctl enable apache2

Verify Apache status:
sudo systemctl status apache2
<img width="1460" height="746" alt="Screenshot 2026-02-04 122839" src="https://github.com/user-attachments/assets/5c5b7fc4-4b12-4868-b134-9f4ae725dc96" />
<img width="1463" height="758" alt="Screenshot 2026-02-04 122924" src="https://github.com/user-attachments/assets/7289ebcd-f42b-462a-aaec-706840ade9b7" />



