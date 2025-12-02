# NGROK ngrok auth token-35hXRX6B9UdSjIR3qNofjKvy0Sd_2draunJLFEDSBG1LHer5J
ngrok config add-authtoken <your_token>
ngrok http 8080
for forwarding add /github-webhook/
git add .
git commit -m "commit"
git push -u origin main
# NAGIOS 1.Pull the nagios docker image
1.docker pull jasonrivers/nagios:latest
2.run nagios
docker run --name nagiosdemo -p 8888:80 jasonrivers/nagios:latest
3.open localhost:8888
Username: nagiosadmin
Password: nagios
# pipeline script 
tools {
    maven 'MAVEN_HOME'
}

stages {

    stage('Git Repo & Clean') {
        steps {
            bat "git clone https://github.com/vaishnavireddy-776/jenkins_web.git"

            // go into folder after cloning
            bat "cd jenkins_web && mvn clean"
        }
    }

    stage('Install') {
        steps {
            bat "cd jenkins_web && mvn install"
        }
    }

    stage('Test') {
        steps {
            bat "cd jenkins_web && mvn test"
        }
    }

    stage('Package') {
        steps {
            bat 'cd jenkins_web && mvn package'
        }
    }
}

# 12. Create Ubuntu VM & Deploy Web App (AWS EC2)
Creating VM
Open AWS Academy Lab.
1.Start lab → Go to EC2 service.
2.Click Launch Instance.
3.Name instance.
4.Choose Ubuntu AMI.
5.Architecture: 64-bit.
6.Instance type: t3.micro.
7.Create key pair (.pem).
8.Create security group → Allow SSH (Anywhere).
9.Storage: 8GB.
10.Number of instances: 2.
11.Launch instance.
12.Connect & Deploy App
13.Select instance → Connect → SSH Client.
14.Open terminal in folder containing .pem file.
15.SSH into instance.
16.Check docker/git installation.
17.If missing:
18.sudo su
19.apt-get update
20.apt-get install docker.io
21.Clone Git repo containing Maven project.
22.Go to project folder.
23.Create Dockerfile if missing.
24.Build image:
25.sudo docker build -t img1 .
26.Run container:
27.sudo docker run -d -p 8081:8080 img1
28.Copy public IP of instance.
29.Open:
http://<public-ip>:8081
30View deployed web app.
