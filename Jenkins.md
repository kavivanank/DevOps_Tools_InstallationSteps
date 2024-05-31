## Installation steps - Jenkins

**NOTE:** JDK required before installation

**Method - 1:**
Installing Jenkins permanently to run on default port 8080, follow the below methods
```
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
```

**Updating system packages & Installing Jenkins**
```
sudo apt-get update -y 
sudo apt-get install jenkins -y
```

**Enabling and starting Jenkins services**
```
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
```
Now, the Jenkins will be available at `<public-ip>:8080`

**Method - 2:**
Temporary installation of Jenkins in the required port number

Select the required version of .jar file from this URL,
https://updates.jenkins.io/download/war/

Right click and copy the URL.
Go to the path, where you are going to download and use the below command to download the war file

```
wget https://updates.jenkins.io/download/war/2.414.2/jenkins.war
```

Run the below command to run the downloaded jenkins application
```
java -jar Jenkins.war  --httpPort=8082
```
