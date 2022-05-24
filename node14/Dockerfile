FROM circleci/node:14

USER root

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip  && \
    sudo ./aws/install

RUN npm i npm@latest -g

RUN node -v
RUN npm -v
RUN python --version
RUN aws --version

USER circleci