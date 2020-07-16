# Maven

Apache Maven is a build automation tool primarily used for building Java applications.

Maven is built using a plugin-based architecture that allows it to make use of any application controllable through standard input.

A plugin for the .NET framework exists and is maintained,and a C/C++ native plugin is maintained for Maven 2.

## Pre-requisites

Install maven on the master and slave nodes.

Install Default jdk

```bash
sudo apt-get install default-jdk
```

Follow the instructions in the [Official Documentation](https://maven.apache.org/)

Make sure the Maven binaries are extacted to a location which is part of the PATH.

To Verify if the maven is correctly installed run

 ```bash
 mvn --version
 ```

### Download maven binaries and extract

In Ubuntu use apt-get install maven

```bash
sudo apt-get install maven -y
```

Note: Make sure to add JAVA_HOME environment variable.
Edit  `/etc/profile` and add the below

```bash
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
```

## Manual Installation

```bash
cd /opt
curl -O http://apachemirror.wuchna.com/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz
tar xvzf apache-maven-3.6.3-bin.tar.gz
sudo ln -s apache-maven-3.6.3-bin.tar.gz maven
```

### Set up Environment Variables

Create a file in `/etc/profile.d` called as maven.sh and the following content

```bash
sudo vim /etc/profile.d/maven.sh
```

```bash
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
export M2_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}
```


##Verify the installation




```bash
mvn --version
```

## Set up in Console.

Once you install maven, go to console in your browser and follow the below steps
1. Click on manage jenkins --> Global Tool Configuration
2. Scroll down to maven and click on maven installations.
3. Add Maven path
