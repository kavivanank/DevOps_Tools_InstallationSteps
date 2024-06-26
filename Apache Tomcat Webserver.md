## Installation steps - JDK and Maven

**NOTE:**  JDK required before installation

**Follow the below steps one by one**

```
cd /opt

sudo wget https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.65/bin/apache-tomcat-9.0.65.tar.gz
```

For different versions of Apache, go to this URL --> https://archive.apache.org/dist/tomcat and select the required version

```
sudo tar -xvf apache-tomcat-9.0.65.tar.gz
```

```
cd /opt/apache-tomcat-9.0.65/conf

sudo vi tomcat-users.xml
```


add-below-line at the end (2nd-last line)
```
<user username="admin" password="admin1234" roles="admin-gui, manager-gui"/>
```
Run the below symbolic links
```
sudo ln -s /opt/apache-tomcat-9.0.65/bin/startup.sh /usr/bin/startTomcat
sudo ln -s /opt/apache-tomcat-9.0.65/bin/shutdown.sh /usr/bin/stopTomcat
```

Edit the below files as mentioned
```
sudo vi /opt/apache-tomcat-9.0.65/webapps/manager/META-INF/context.xml```

---comment the below line--- 
<!-- Valve className="org.apache.catalina.valves.RemoteAddrValve"
  allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" /> -->
```
```
sudo vi /opt/apache-tomcat-9.0.65/webapps/host-manager/META-INF/context.xml
---comment the below line---
<!-- Valve className="org.apache.catalina.valves.RemoteAddrValve"
  allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" /> -->
```

**Start tomcat** 
```
sudo startTomcat
```

**For running Tomcat as a non-root user,**
```
chown -R ubuntu /opt/apache-tomcat-9.0.65
chmod -R 757 /opt/apache-tomcat-9.0.65
```

**To deploy a maven build application and make it available on internet, copy the .war file to webapps directory for deploying the application**
```
sudo cp target/<application-name>.war /opt/apache-tomcat-9.0.65/webapps/
(or)
sudo cp target/*.war /opt/apache-tomcat-9.0.65/webapps/
```
