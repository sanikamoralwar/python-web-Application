# Python Web Application Deployment on Ec2
### Introduction
This project demonstrates how to deploy a Python web application on a cloud server using Amazon EC2. It
covers the complete process from launching a virtual server to running the application successfully.<br>
The goal of this project is to gain hands-on experience with cloud computing, Linux commands, and Python
environment setup.
### Architecture Diagram
![](./img/Architecture%20diagram.png)
## Steps I Followed
### 1.launching an ec2 instance
![](./img/py-1.png)
### 2.Connect using ssh<br>
ssh -i your-key.pem ec2-user@your-public-ip
![](./img/py-2.png)
### 3.Installation of PYTHON
sudo yum update -y<br>
sudo yum install python3 -y
![](./img/py-3.png)
* verify version:<br>
python3 --version<br>
### 4.Installation of pip
sudo yum install python3-pip -y
![](./img/py-4.png)
* Verify pip:<br>
pip3 --version
### 5.Clone the Repository<br>
git clone url<br>
cd pythonapp
![](./img/py-5.png)
### 6.Create Virtual Environment<br>
python3 -m venv myenv
![](./img/py-6.png)
### 7.Activate virtual environment<br>
bash myenv/bin/activates
![](./img/py-7.png)
### 8.Install dependencies<br>
pip install -r requirements.txt<br>
python3 app.pp
![](./img/py-8.png)
### 9. Start the Application
sudo python3 app.py
![](./img/py-9.1.png)
### 10.Access the Application<br>
public ip : port<br>
port no -> 5000
![](./img/py-9.2.png)
### 11.Run the Application in the Background
sudo gunicorn --bind 0.0.0.0:5000 app:app --daemon
![](./img/py-10.1.png)
![](./img/py-10.2.png)
### Key Features
* Deployment on AWS EC2<br>
* Complete setup from scratch<br>
* Virtual environment usage<br>
* Dependency management with pip
### Challenges Faced
* Connecting securely using SSH<br>
* Managing Linux commands<br>
* Setting up Python environment correctly
### Project Summary
This project successfully demonstrates the deployment of a Python web application on a cloud platform.
Starting from launching an EC2 instance, the process includes installing required tools, configuring the
environment, and running the application. It provides practical experience in cloud computing, server
management, and backend deployment, making it a strong foundation for real-world DevOps and backend
development tasks