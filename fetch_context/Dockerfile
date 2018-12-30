FROM jetware/base_os:alpine3.8

ARG OWNER
ARG NAME
ARG VERSION

COPY fetch /fetch
RUN /fetch $OWNER $NAME $VERSION
