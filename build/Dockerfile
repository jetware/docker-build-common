FROM scratch
COPY --from=jet /jet /jet

ARG OS
COPY --from=jetware/base_os:$OS / /

RUN chown -R jet /jet; \
    { echo "jet ALL=NOPASSWD: ALL"; echo "Defaults:jet !requiretty"; } > /etc/sudoers.d/99-jet-tmp; \
	echo "/jet/own/bin/run /jet/own/bin/fasten" | su jet -s /bin/sh; \
	rm -f /etc/sudoers.d/99-jet-tmp

WORKDIR /jet
USER jet
VOLUME ["/jet/prs"]
ENTRYPOINT ["/jet/login"]
CMD ["main"]
