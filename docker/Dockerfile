FROM nginx

RUN apt-get update && \
    apt-get install --no-install-recommends --no-install-suggests -y logrotate && \
    rm -rf /var/lib/apt/lists/*