# herovired_jenkins_project
---------------------------------------
## Jenkins Installation
- ### Creation of EC2
  - Click on Search bar and type EC2 instance and select EC2 option
    ![image](https://github.com/user-attachments/assets/66eff39f-a019-47f4-a4f8-70b1551544dd)

  - Click the Launch instance button.
  ![image](https://github.com/user-attachments/assets/d8957fff-481e-401f-81fc-9ae595b07075)

  - Provide the information like
    - Name for ec2 instance
    - Select AMI(Select ubuntu 24)
    - Select Instance Type(t2.micro)
    - Create or Select existing Key pair
    - In Network settings, Create Security Group
      - Enable Port 22, 8080
    - Click on Launch EC2
  ![image](https://github.com/user-attachments/assets/aa1c0d73-1894-44c2-9e4a-b0b79e535578)


  - ### Jenkins installation
    - Run below commands

```
sudo apt update
sudo apt install openjdk-17-jdk -y

```

```
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
```

```
echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
```

```
sudo apt-get update
```

```
sudo apt-get install jenkins
```

![image](https://github.com/user-attachments/assets/ad797145-6481-402f-b5d9-b4374472d2ca)

- Please provide password by using given and click on continue

![image](https://github.com/user-attachments/assets/a2b61548-1efd-4bee-9955-8218ae6ef321)

![image](https://github.com/user-attachments/assets/120263da-1e08-4a07-94ff-535e580fc17f)

- Select **Install Suggested plugins** option
  ![image](https://github.com/user-attachments/assets/a75e006e-28c1-4167-9a36-58b6aa3405f3)

- Creation of Admin user: Provide information like Username, Password, Confirm Password, Full name and   E-mail address
    ![image](https://github.com/user-attachments/assets/e70bb499-77a7-4115-b1ab-7b0e0e248190)

![image](https://github.com/user-attachments/assets/3a2acbfd-1b76-4377-8fce-1fa1aa663804)

## Application Installation

```
#sudo apt install -y python3 python3-pip
```
```
#pip install flask
```
```
#python3 app.py
```
![image](https://github.com/user-attachments/assets/50d63517-8526-4ac6-8ba4-388492bc058d)

![image](https://github.com/user-attachments/assets/106e14cc-8cf1-4e29-ae2b-5126e99e296d)

Add extra code in app.py

![image](https://github.com/user-attachments/assets/32c36fda-0cad-4d92-9584-8b3b1cba4b8d)

![image](https://github.com/user-attachments/assets/f4f8ae85-ea6d-452d-b914-fd5f77ac4c83)























  


     
