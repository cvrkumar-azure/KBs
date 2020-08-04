

# CentOS


`sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins.io/redhat-stable/jenkins.repo`

`sudo rpm --import http://pkg.jenkins.io/redhat-stable/jenkins.io.key`

`sudo yum install jenkins java-1.8.0-openjdk –y`

`sudo systemctl start jenkins`

`sudo systemctl enable jenkins`