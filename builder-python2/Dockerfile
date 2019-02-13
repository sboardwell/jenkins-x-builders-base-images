ARG FROM_IMAGE=to-be-set-in-the-skaffold-yaml
ARG FROM_VERSION=to-be-set-in-the-skaffold-yaml
FROM $FROM_IMAGE:$FROM_VERSION

RUN yum install -y python python-libs python-devel python-pip \
    && yum clean all

CMD ["python", "--version"]
