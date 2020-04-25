FROM jenkins/jenkins:lts

USER root

# install git, python and poetry
RUN apt-get update
RUN apt-get install git
RUN apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev
RUN git clone https://github.com/pyenv/pyenv.git ~/.pyenv
ENV PATH "/root/.pyenv/shims/:/root/.pyenv/bin/:$PATH"
RUN pyenv install 3.7.2
RUN pyenv global 3.7.2
RUN pip install poetry

# configuration as code
COPY plugins.txt /usr/share/jenkins/plugins.txt
COPY jenkins.yaml /var/jenkins_home/jenkins.yaml
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/plugins.txt
