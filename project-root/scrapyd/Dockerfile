FROM python:3.10-slim

WORKDIR /app

# 安装 scrapyd
RUN pip install --no-cache-dir scrapyd

# 开放默认端口
EXPOSE 6800

# 启动 scrapyd 服务
CMD ["scrapyd"]
