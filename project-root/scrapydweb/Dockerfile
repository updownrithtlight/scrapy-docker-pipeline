FROM python:3.10-slim

WORKDIR /app

COPY scrapydweb_settings_v11.py /app/

RUN pip install --no-cache-dir scrapydweb

EXPOSE 5000

CMD ["scrapydweb"]
