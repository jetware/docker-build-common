ARG OS
FROM scratch
COPY --from=jet /jet /jet

FROM jetware/base_os:$OS as base_os
COPY --from=base_os / /

RUN chown -R jet /jet; \
    { echo "jet ALL=NOPASSWD: ALL"; echo "Defaults:jet !requiretty"; } > /etc/sudoers.d/99-jet-tmp; \
	echo "/jet/own/bin/run /jet/own/bin/fasten" | su jet -s /bin/sh; \
	rm -f /etc/sudoers.d/99-jet-tmp

WORKDIR /jet
USER jet
VOLUME ["/jet/prs"]
ENTRYPOINT ["/jet/login"]
CMD ["main"]
