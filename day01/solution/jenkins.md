### Install jenkins in your local system
Install Jenkins on windows
```docker
# download jdk/jre and install as well as set the path in enviraonment variable.
# download it from https://www.jenkins.io/doc/book/installing/windows/
# and install the exe file
```
Install Jenkins on linux system
```
# At first check java is installed or not
java

# If java is not Installed install it
sudo apt install openjdk-11-jdk

# set jenkins package  in your system
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
  
# set signeture
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
  
# update your system packages
sudo apt-get update

# install jenkins
sudo apt-get install jenkins
```

### Dashboard Overview

### Create a free style job
### Build it reconfigured it
### Search panel overview
### Configuration overview
### Manage plugin overview
### Install a plugin
### Configure the plugin
### Remove/Uninstall the plugin