
## Step 1: Ensure all the necessary plugins are installed in Jenkins server
- [ ] Docker Pipeline
- [ ] SonarQube Scanner
- [ ] Quality Gates

## Step 2: Install Docker, Java8, Java11 & Trivy
```
$ sudo ./setup.sh
```

## Step 3: Install Sonrqube on the t2.medium server
```
$ sudo apt update
$ sudo apt install -y docker.io
$ sudo usermod -a -G docker ubuntu
$ sudo docker run -d --name sonar -p 9000:9000 sonarqube:lts-community
```

## Step 4: Add necessary credentials
- [ ] Generate Sonarqube token of type "global analysis token" and add it as Jenkins credential of type "secret text"
- [ ] Add dockerhub credentials as username/password type

## Step 5: Enable Sonarqube webhook for Quality Gates & Install dependency-check plugin
- [ ] Generate webhook & add the Jenkins URL as follows - http://URL:8080/sonarqube-webhook/



Results:
<img width="1882" height="821" alt="image" src="https://github.com/user-attachments/assets/61c38f92-2ab4-4562-9912-f95d9da47ea0" />

<img width="1857" height="532" alt="image" src="https://github.com/user-attachments/assets/646824c3-a340-4cfa-bdf1-9a616cdd6564" />


Pipeline with security testing in parallel stages  (Intentionally made the quality gate stage and Trivy scan stage pass to execute all the stages)
<img width="1870" height="828" alt="image" src="https://github.com/user-attachments/assets/a19f5d12-1c64-4be8-a38d-7343a42ba138" />

<img width="1860" height="551" alt="image" src="https://github.com/user-attachments/assets/faa497d4-d012-492d-a7c9-effbaae5487b" />
