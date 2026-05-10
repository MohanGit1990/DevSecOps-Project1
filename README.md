# DevSecOps-Project1
CodeCoverage,SCA,SAST,DAST,QualityGate,ImageScan,SmokeTest,EmailNotification


1. Create 3 servers - SonarQube, Jenkins, Application

2. Jenkins server
   Install Java versions which are required (1 for Jenkins server, another for application to run) if multiple versions are required
   Install Jenkins
   Install the plugins
   create credentials to login to sonarqube
   Update system Configuration to indicate the sonarqube url and creds to jenkins since its webapp (if its cli tool you need to update in the Manage Jenkins -> tools section)
   


4. SonarQube server
   Install Docker and build sonarqube container
   Create tokens for other applications to user sonarqube
