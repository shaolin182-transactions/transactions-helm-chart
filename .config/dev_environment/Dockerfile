FROM docker.io/ubuntu:24.04

# Install Python
RUN apt-get update
RUN apt-get -y install wget python3 python3-pip


# Install HELM
RUN wget -O- https://packages.buildkite.com/helm-linux/helm-debian/gpgkey | gpg --dearmor | tee /usr/share/keyrings/helm.gpg > /dev/null
RUN apt-get install apt-transport-https --yes
RUN sh -c 'echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://packages.buildkite.com/helm-linux/helm-debian/any/ any main" >> /etc/apt/sources.list.d/helm-stable-debian.list'
RUN apt-get update
RUN apt-get install helm

ENV PATH=$PATH:/root/.local/bin

RUN mkdir -p /app