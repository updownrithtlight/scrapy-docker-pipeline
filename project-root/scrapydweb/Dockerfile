FROM python:3.10-slim

WORKDIR /app

# 安装 scrapydweb
RUN pip install --no-cache-dir scrapydweb

# 复制默认配置（可选）
RUN mkdir -p /root/.scrapydweb

# 开放默认端口
EXPOSE 5000

# 启动 scrapydweb
CMD ["scrapydweb"]
