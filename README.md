
# Web Application Deployment on EC2

## Project Overview

This project demonstrates how to deploy a basic web application on an **AWS EC2 instance** using **Apache2** on **Ubuntu Linux**. The setup includes launching an EC2 instance, configuring security groups, installing a web server, and verifying web access.

---

## Step 1: Create an EC2 Instance

1. Navigate to **AWS Console → EC2 → Launch Instance**.
2. Choose an **Amazon Machine Image (AMI)**:

   * Ubuntu Server **20.04 LTS** or **22.04 LTS**
3. Select an **Instance Type**:

   * `t2.micro` (Free Tier eligible)
4. Create or select an existing **Key Pair** for SSH access.

 <img width="1919" height="777" alt="EC2 Launch" src="https://github.com/user-attachments/assets/75b9d5f2-d9d8-499d-9f01-ab88d468b7f3" /> <img width="1912" height="712" alt="EC2 AMI Selection" src="https://github.com/user-attachments/assets/ca831f3e-e6e0-4f8c-b7c0-cabe6847436c" />

---

## Step 2: Configure Security Group (Firewall Rules)

Configure the EC2 security group to allow inbound traffic as shown below:

| Protocol | Port | Source               |
| -------- | ---- | -------------------- |
| SSH      | 22   | Your IP              |
| HTTP     | 80   | Anywhere (0.0.0.0/0) |


 <img width="1919" height="755" alt="Security Group Rules" src="https://github.com/user-attachments/assets/58f878b7-405e-4d70-bdab-f7bcadc470f6" />

---

## Step 3: Connect to EC2 Using SSH

Use SSH to connect to your instance from your local machine or AWS console.


<img width="1919" height="786" alt="SSH Connect" src="https://github.com/user-attachments/assets/bce4cfaf-51b1-4430-9154-327d3e533821" /> <img width="1909" height="751" alt="SSH Terminal" src="https://github.com/user-attachments/assets/15014374-5bd4-438b-8935-d9ce122b9880" /> <img width="1471" height="746" alt="Ubuntu Login" src="https://github.com/user-attachments/assets/732c5330-0f3e-4a1e-a571-42807cd06c4f" />

---

## Step 4: Install and Start Apache2 Web Server

### Update the package list

```bash
sudo apt update
```

### Install Apache2

```bash
sudo apt install apache2 -y
```

### Start and enable Apache

```bash
sudo systemctl start apache2
sudo systemctl enable apache2
```

### Verify Apache status

```bash
sudo systemctl status apache2
```

 <img width="1460" height="746" alt="Apache Install" src="https://github.com/user-attachments/assets/5c5b7fc4-4b12-4868-b134-9f4ae725dc96" /> <img width="1463" height="758" alt="Apache Status" src="https://github.com/user-attachments/assets/7289ebcd-f42b-462a-aaec-706840ade9b7" /> <img width="1465" height="751" alt="Apache Running" src="https://github.com/user-attachments/assets/66869717-b708-46f4-a52b-da70c3d9a05d" />

---

## Step 5: Test HTTP Access

1. Open a web browser.
2. Enter the **Public IP address** of the EC2 instance.
3. Confirm that the **Apache2 default page** is displayed.

 <img width="1907" height="953" alt="Apache Default Page" src="https://github.com/user-attachments/assets/0d35bab3-0496-4860-a6db-3666b0e39957" />

---

## Step 6: Deploy a Sample Web Application

Replace the default Apache content with a sample web application or custom HTML files.
Save and exit the file.
Refresh the browser to view the deployed application.


<img width="1460" height="513" alt="Web App Deployment" src="https://github.com/user-attachments/assets/8dd6ba95-4569-4b45-a0bf-323486f66495" />
<img width="1915" height="673" alt="Screenshot 2026-02-04 124408" src="https://github.com/user-attachments/assets/5fee71d4-b7bb-407a-8b77-9f4409f6ab97" />


---

## Conclusion

In this project, we successfully:

* Launched an EC2 instance
* Configured security groups
* Installed and configured Apache2
* Deployed and accessed a web application over HTTP





