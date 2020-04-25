FROM jenkins/jenkins:lts
# configuration as code
COPY plugins.txt /usr/share/jenkins/plugins.txt
COPY jenkins.yaml /var/jenkins_home/jenkins.yaml
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/plugins.txt
