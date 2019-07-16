FROM ubuntu:latest
EXPOSE 4200
USER root
WORKDIR /opt/angular

RUN apt-get update
RUN apt-get install -y git
RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN apt-get install -y nodejs
RUN apt-get install -y build-essential

RUN useradd -m -s /bin/bash angular
RUN usermod -aG sudo angular
RUN chown -R angular:angular .
RUN NG_CLI_ANALYTICS=ci npm install -g @angular/cli

USER angular
RUN git clone https://github.com/yamileon/poolmanage-ui.git

WORKDIR /opt/angular/poolmanage-ui
RUN git checkout furr-dev2
RUN yes | npm install

ENTRYPOINT ["/usr/bin/ng", "serve", "--host", "0.0.0.0"]
