ARG FROM_IMAGE=to-be-set-in-the-skaffold-yaml
ARG FROM_VERSION=to-be-set-in-the-skaffold-yaml
FROM $FROM_IMAGE:$FROM_VERSION

RUN yum install -y https://centos7.iuscommunity.org/ius-release.rpm \
    && yum update  -y \
    && yum install -y python36u python36u-libs python36u-devel python36u-pip \
    && yum clean all
RUN ln -s /usr/bin/python3.6 /usr/bin/python3

CMD ["python3", "--version"]
