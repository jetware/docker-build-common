FROM jetware/base_fetch

ARG OWNER
ARG NAME
ARG VERSION

RUN /fetch $OWNER $NAME $VERSION && rm -f /fetch && chown -R 999:0 /jet
