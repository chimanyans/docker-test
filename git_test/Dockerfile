FROM node:8

RUN apt-get update
RUN apt-get install -y git

# Make ssh dir
RUN mkdir /root/.ssh/

# Copy over private key, and set permissions
ADD /ssh/id_rsa /root/.ssh/id_rsa

# Create known_hosts
RUN touch /root/.ssh/known_hosts
# Add github key
RUN ssh-keyscan github.com >> /root/.ssh/known_hosts

RUN git clone git@github.com:PUBLIQNetwork/publiq-api.git
