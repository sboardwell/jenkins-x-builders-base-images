ARG FROM_IMAGE=to-be-set-in-the-skaffold-yaml
ARG FROM_VERSION=to-be-set-in-the-skaffold-yaml
FROM $FROM_IMAGE:$FROM_VERSION

# Set JDK to be 32bit
COPY set_java $M2
RUN $M2/set_java && rm $M2/set_java
