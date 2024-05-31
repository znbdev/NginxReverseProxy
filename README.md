# Nginx reverse proxy

This is a simple example of how to set up a reverse proxy using Nginx and Docker.

# Usage

### 在启动 Docker 容器之前，运行以下命令初始获取 SSL 证书：

```shell
docker-compose run --rm certbot certonly --webroot --webroot-path=/var/www/certbot --email your-email@example.com --agree-tos --no-eff-email -d yourdomain.com
```

### 确保将 yourdomain.com 替换为你的域名，your-email@example.com 替换为你的电子邮件地址。

### 启动 Docker 容器：

运行以下命令启动 Nginx 和 Certbot 容器：

```shell
docker-compose up -d
```

### 访问你的域名，你应该会看到 Nginx 服务器的欢迎页面。
