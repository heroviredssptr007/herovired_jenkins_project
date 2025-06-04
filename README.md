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

## Creation of Jenkins Job
- ### Github password creation
  - Go to Profile and Select Setting
    ![image](https://github.com/user-attachments/assets/2ee688c3-a45f-461e-8823-39a1f8896025)

  - Select the Developer setting

    ![image](https://github.com/user-attachments/assets/ceb599ca-477f-4f58-ae5b-4cbfe155b620)

  -  Click on Personal access tokens and select Tokens(classic), Click Generate new token and select Generate new token(classic)

    ![image](https://github.com/user-attachments/assets/2a0b8702-841c-4875-8738-ba3433491fdb)

  - Provide the name to the token, select all the permission required and Click on Generate Token, Copy and Keep it safe the token

    ![image](https://github.com/user-attachments/assets/5eee2738-0462-42e8-a714-b1fcd8fbd552)

    ![image](https://github.com/user-attachments/assets/dfc18817-98dc-4650-bb12-4413d2e42a0e)

- ### Adding github and ssh credentials
  - Go to Manage Jenkins ->  Select Credentials -> Click on System -> Click on Global Credentials -> Click on Add Credentials

    ![image](https://github.com/user-attachments/assets/a19b041d-349d-4f14-bf9d-42be25b4c1ca)

  - Select Username and Password option and provide Username, Password and click on Create

    ![image](https://github.com/user-attachments/assets/50584c6a-7cbf-45f6-b41d-0d2135e671ba)

  - Adding SSH credentials
    - Click on Add credentials and Select `SSH username with private key` option, Provide information like Username and private key and click on Create
      ![image](https://github.com/user-attachments/assets/89b167e8-e6d1-44ac-8a11-6bfeabc8d5fa)

- ### Creation of Jenkins Job
  - Click on Create job, Provide name and select Pipeline and click OK

    ![image](https://github.com/user-attachments/assets/9cfe2c83-ef19-4a3d-a94b-f46de61b8693)

  - In General section, **Pipeline**, Select `Pipeline script from SCM`, In SCM select GIT and provide the repository path, In Credentials select github credential. In Branch Specifier provide Branch as `main` and click on save. Click on Build now option

    ![image](https://github.com/user-attachments/assets/1a272184-993b-4ad6-a63b-39ada95baf39)

    ![image](https://github.com/user-attachments/assets/608d649c-3fd1-442d-9325-02cc31d86251)

    ![image](https://github.com/user-attachments/assets/36ea4174-23b6-4550-ba79-f3cce36d2e75)


    


  

    
    


      

    




    



























  


     
