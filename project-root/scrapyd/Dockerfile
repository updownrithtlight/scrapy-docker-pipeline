FROM python:3.10-slim

RUN apt-get update && apt-get install -y \
    gcc libffi-dev libssl-dev libxml2-dev libxslt1-dev \
 && pip install --no-cache-dir scrapyd \
 && apt-get purge -y gcc \
 && apt-get autoremove -y \
 && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY scrapyd.conf /etc/scrapyd/

RUN mkdir -p /var/lib/scrapyd/logs \
             /var/lib/scrapyd/items \
             /var/lib/scrapyd/dbs \
             /src/eggs

VOLUME ["/var/lib/scrapyd", "/src/eggs"]

EXPOSE 6800

CMD ["scrapyd", "--pidfile="]
