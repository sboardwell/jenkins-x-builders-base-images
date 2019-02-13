ARG FROM_IMAGE=to-be-set-in-the-skaffold-yaml
ARG FROM_VERSION=to-be-set-in-the-skaffold-yaml
FROM $FROM_IMAGE:$FROM_VERSION

ARG YARN_VERSION=1.3.2
ARG NODE_VERSION=to-be-set-in-the-root-skaffold-file

RUN yum install -y gcc-c++ make bzip2 GConf2 gtk2 chromedriver chromium xorg-x11-server-Xvfb \
    && yum clean all

# Yarn
ENV YARN_VERSION ${YARN_VERSION}
RUN curl -f -L -o /tmp/yarn.tgz https://github.com/yarnpkg/yarn/releases/download/v${YARN_VERSION}/yarn-v${YARN_VERSION}.tar.gz && \	
	tar xf /tmp/yarn.tgz && \
	mv yarn-v${YARN_VERSION} /opt/yarn && \
	ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn && \
    rm -f /tmp/yarn.tgz

RUN curl -f --silent --location https://rpm.nodesource.com/setup_${NODE_VERSION} | bash - && \
    yum install -y nodejs \
    && yum clean all

RUN npm i -g watch-cli vsce typescript

