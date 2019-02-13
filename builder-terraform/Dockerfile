ARG FROM_IMAGE=to-be-set-in-the-skaffold-yaml
ARG FROM_VERSION=to-be-set-in-the-skaffold-yaml
FROM $FROM_IMAGE:$FROM_VERSION

ENV TERRAFORM 0.11.11
RUN wget -q https://releases.hashicorp.com/terraform/${TERRAFORM}/terraform_${TERRAFORM}_linux_amd64.zip && \
  unzip terraform_${TERRAFORM}_linux_amd64.zip && \
  chmod +x terraform && mv terraform /usr/bin/terraform && rm terraform_${TERRAFORM}_linux_amd64.zip

ENV TERRAGRUNT_VERSION 0.17.4
RUN curl -f -Lo terragrunt https://github.com/gruntwork-io/terragrunt/releases/download/v${TERRAGRUNT_VERSION}/terragrunt_linux_amd64 && \
  chmod +x terragrunt && \
  mv terragrunt /usr/bin

ENV PATH $PATH:/usr/local/
